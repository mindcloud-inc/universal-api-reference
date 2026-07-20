# Vaiz: Native API Reference

A consolidated summary of Vaiz's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://docs-python-sdk.vaiz.com/api-reference/overview
- **API base URL:** `https://api.vaiz.com/v4`

## Authentication

### Personal Access Token

Authenticate to Vaiz with a personal access token. Optionally provide a space ID when your workspace requires the current-space-id header.

### Credentials

- **API Key:** `apiKey` · required
- **Space ID:** `spaceId` · optional · Optional Vaiz space ID used when requests must send the current-space-id header.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://vaiz.com/help/tutorials/how-to-generate-personal-access-token)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Reaction](actions/add-reaction.md) | `POST reactToComment` | [docs](https://docs-python-sdk.vaiz.com/api-reference/comments) |
| [Append Document](actions/append-document.md) | `POST appendDocument` | [docs](https://docs-python-sdk.vaiz.com/api-reference/document-structure) |
| [Append JSON Document](actions/append-json-document.md) | `POST appendJSONDocument` | [docs](https://docs-python-sdk.vaiz.com/api-reference/document-structure) |
| [Create Comment](actions/create-comment.md) | `POST postComment` | [docs](https://docs-python-sdk.vaiz.com/api-reference/comments) |
| [Create Document](actions/create-document.md) | `POST createDocument` | [docs](https://docs-python-sdk.vaiz.com/api-reference/documents) |
| [Create Milestone](actions/create-milestone.md) | `POST createMilestone` | [docs](https://docs-python-sdk.vaiz.com/api-reference/milestones) |
| [Create Task](actions/create-task.md) | `POST createTask` | [docs](https://docs-python-sdk.vaiz.com/api-reference/tasks) |
| [Delete Comment](actions/delete-comment.md) | `POST deleteComment` | [docs](https://docs-python-sdk.vaiz.com/api-reference/comments) |
| [Get Board](actions/get-board.md) | `POST getBoard` | [docs](https://docs-python-sdk.vaiz.com/api-reference/boards) |
| [Get JSON Document](actions/get-json-document.md) | `POST getJSONDocument` | [docs](https://docs-python-sdk.vaiz.com/api-reference/document-structure) |
| [Get Milestone](actions/get-milestone.md) | `POST getMilestone` | [docs](https://docs-python-sdk.vaiz.com/api-reference/milestones) |
| [Get Profile](actions/get-profile.md) | `POST getProfile` | [docs](https://docs-python-sdk.vaiz.com/api-reference/profile) |
| [Get Project](actions/get-project.md) | `POST getProject` | [docs](https://docs-python-sdk.vaiz.com/api-reference/projects) |
| [Get Space](actions/get-space.md) | `POST getSpace` | [docs](https://docs-python-sdk.vaiz.com/api-reference/spaces) |
| [Get Task](actions/get-task.md) | `POST getTask` | [docs](https://docs-python-sdk.vaiz.com/api-reference/tasks) |
| [List Boards](actions/list-boards.md) | `POST getBoards` | [docs](https://docs-python-sdk.vaiz.com/api-reference/boards) |
| [List Comments](actions/list-comments.md) | `POST getComments` | [docs](https://docs-python-sdk.vaiz.com/api-reference/comments) |
| [List Documents](actions/list-documents.md) | `POST getDocuments` | [docs](https://docs-python-sdk.vaiz.com/api-reference/documents) |
| [List Milestones](actions/list-milestones.md) | `POST getMilestones` | [docs](https://docs-python-sdk.vaiz.com/api-reference/milestones) |
| [List Projects](actions/list-projects.md) | `POST getProjects` | [docs](https://docs-python-sdk.vaiz.com/api-reference/projects) |
| [List Space Members](actions/list-space-members.md) | `POST getSpaceMembers` | [docs](https://docs-python-sdk.vaiz.com/api-reference/members) |
| [List Tasks](actions/list-tasks.md) | `POST getTasks` | [docs](https://docs-python-sdk.vaiz.com/api-reference/tasks) |
| [Move Tasks](actions/move-tasks.md) | `POST moveTasks` | [docs](https://docs-python-sdk.vaiz.com/api-reference/tasks) |
| [Replace Document](actions/replace-document.md) | `POST replaceDocument` | [docs](https://docs-python-sdk.vaiz.com/api-reference/document-structure) |
| [Replace JSON Document](actions/replace-json-document.md) | `POST replaceJSONDocument` | [docs](https://docs-python-sdk.vaiz.com/api-reference/document-structure) |
| [Toggle Milestone](actions/toggle-milestone.md) | `POST toggleMilestone` | [docs](https://docs-python-sdk.vaiz.com/api-reference/milestones) |
| [Update Comment](actions/update-comment.md) | `POST editComment` | [docs](https://docs-python-sdk.vaiz.com/api-reference/comments) |
| [Update Document](actions/update-document.md) | `POST editDocument` | [docs](https://docs-python-sdk.vaiz.com/api-reference/documents) |
| [Update Milestone](actions/update-milestone.md) | `POST editMilestone` | [docs](https://docs-python-sdk.vaiz.com/api-reference/milestones) |
| [Update Task](actions/update-task.md) | `POST editTask` | [docs](https://docs-python-sdk.vaiz.com/api-reference/tasks) |
