# Wrike GraphQL Schema

## Overview

This document describes a conceptual GraphQL schema for the Wrike work management and collaboration platform. Wrike exposes a REST API v4 at https://www.wrike.com/api/v4, and this schema models the equivalent types, queries, mutations, and subscriptions that a GraphQL layer over that API would provide.

The Wrike API covers tasks, folders, projects, contacts, workflows, custom fields, time tracking, timesheets, approvals, attachments, audit logs, webhooks, and automation rules. Authentication uses OAuth 2.0 or permanent access tokens.

Reference: https://developers.wrike.com/api/v4/

## Schema Source

- **Provider**: Wrike
- **API Version**: v4
- **Base URL**: https://www.wrike.com/api/v4
- **Developer Docs**: https://developers.wrike.com/
- **Schema File**: wrike-schema.graphql
- **Schema Type**: Conceptual (derived from REST API documentation)

## Type Summary

| Category | Types |
|---|---|
| Account & Auth | Account, AccountDetails, UserType, APIKey, Token |
| Users & Contacts | User, UserDetails, UserRole, UserProfile, Contact, Invitation, TeamMember |
| Groups & Spaces | Group, GroupDetails, Space, SpaceDetails, SpaceAccess |
| Tasks | Task, TaskDetails, TaskStatus, TaskImportance, TaskDate, TaskAssignees, TaskComment, TaskDependency, TaskCustomField, TaskCustomStatus |
| Folders & Projects | Folder, FolderDetails, FolderTree, Project, ProjectDetails, ProjectStatus, BlueprintTemplate, FolderTemplate |
| Workflows | Workflow, WorkflowStage, WorkflowTransition, CustomStatus, AutomationRule, RuleCondition, RuleAction |
| Comments & Attachments | Comment, CommentDetails, Attachment, AttachmentMetadata |
| Timeline & Dependencies | Timeline, TaskTimeline, ProjectTimeline, Dependency, DependencyType |
| Time Tracking | TimesheetEntry, TimesheetDetails, HourRate |
| Reporting & Budget | Report, BudgetSummary, BillingItem, Activity, ActivityType, Stream, StreamFilter |
| Approvals & Review | ApprovalWorkflow, Approval, ReviewVersion, ReviewComment |
| Webhooks | Webhook |

## Queries

- `account`: Fetch the current account and its details.
- `users`: List users in the account with optional filters.
- `user(id: ID!)`: Fetch a single user by ID.
- `contacts`: List contacts visible to the current user.
- `groups`: List groups in the account.
- `spaces`: List spaces available in the account.
- `folders(spaceId: ID, parentId: ID)`: List folders optionally filtered by space or parent.
- `folder(id: ID!)`: Fetch a single folder by ID.
- `folderTree(id: ID!)`: Fetch a folder and all its descendants.
- `projects(spaceId: ID, status: ProjectStatus)`: List projects with optional filters.
- `project(id: ID!)`: Fetch a single project by ID.
- `tasks(folderId: ID, status: TaskStatus, assigneeId: ID, importance: TaskImportance)`: List tasks with filters.
- `task(id: ID!)`: Fetch a single task by ID.
- `workflows`: List all workflows defined in the account.
- `workflow(id: ID!)`: Fetch a single workflow by ID.
- `comments(taskId: ID, folderId: ID)`: List comments on a task or folder.
- `attachments(taskId: ID, folderId: ID)`: List attachments on a task or folder.
- `timesheetEntries(userId: ID, startDate: String, endDate: String)`: Query timesheet entries.
- `reports`: List available reports.
- `approvals(taskId: ID)`: List approvals on a task.
- `webhooks`: List webhooks registered for the account.
- `activities(streamId: ID)`: Fetch activity stream entries.
- `dependencies(taskId: ID!)`: List dependencies for a task.
- `automationRules`: List automation rules defined in the account.

## Mutations

- `createTask(input: CreateTaskInput!)`: Create a new task in a folder or project.
- `updateTask(id: ID!, input: UpdateTaskInput!)`: Update task fields, status, or assignees.
- `deleteTask(id: ID!)`: Delete a task.
- `createFolder(input: CreateFolderInput!)`: Create a folder.
- `updateFolder(id: ID!, input: UpdateFolderInput!)`: Update a folder.
- `deleteFolder(id: ID!)`: Delete a folder.
- `createProject(input: CreateProjectInput!)`: Create a project (folder with project metadata).
- `updateProject(id: ID!, input: UpdateProjectInput!)`: Update a project.
- `deleteProject(id: ID!)`: Delete a project.
- `createComment(taskId: ID!, text: String!)`: Add a comment to a task.
- `updateComment(id: ID!, text: String!)`: Edit an existing comment.
- `deleteComment(id: ID!)`: Delete a comment.
- `uploadAttachment(taskId: ID!, file: Upload!)`: Upload an attachment to a task.
- `deleteAttachment(id: ID!)`: Delete an attachment.
- `logTime(input: TimesheetEntryInput!)`: Log time against a task.
- `updateTimesheetEntry(id: ID!, input: UpdateTimesheetInput!)`: Update a time entry.
- `deleteTimesheetEntry(id: ID!)`: Delete a time entry.
- `createWebhook(input: WebhookInput!)`: Register a new webhook.
- `updateWebhook(id: ID!, input: WebhookInput!)`: Update a webhook.
- `deleteWebhook(id: ID!)`: Delete a webhook.
- `inviteUser(input: InvitationInput!)`: Invite a user to the account.
- `createGroup(input: GroupInput!)`: Create a user group.
- `updateGroup(id: ID!, input: GroupInput!)`: Update a group.
- `createAutomationRule(input: AutomationRuleInput!)`: Create an automation rule.
- `updateAutomationRule(id: ID!, input: AutomationRuleInput!)`: Update an automation rule.
- `deleteAutomationRule(id: ID!)`: Delete an automation rule.
- `submitApproval(taskId: ID!, decision: ApprovalDecision!, comment: String)`: Submit an approval decision.

## Subscriptions

- `taskUpdated(folderId: ID)`: Real-time updates when tasks change within a folder or project.
- `commentAdded(taskId: ID!)`: Fires when a comment is added to a task.
- `attachmentUploaded(taskId: ID!)`: Fires when an attachment is uploaded.
- `approvalUpdated(taskId: ID!)`: Fires when an approval decision changes.
- `webhookEvent(accountId: ID!)`: Proxies Wrike webhook payloads as GraphQL subscription events.

## Authentication

Requests must include a valid OAuth 2.0 bearer token or permanent access token in the `Authorization: Bearer <token>` header. Scopes control access to tasks, projects, time tracking, contacts, and admin features.

## Notes

- This is a conceptual schema. Wrike does not currently expose a native GraphQL endpoint.
- Types and field names are derived from the Wrike REST API v4 documentation at https://developers.wrike.com/api/v4/.
- IDs use Wrike's Base64-encoded identifier format internally; the schema exposes them as `ID` scalars.
- Dates and times are represented as ISO 8601 strings.
- Custom fields are modeled as a union of scalar value types to accommodate Wrike's flexible custom field system.
