# <img src="https://images.mindcloud.co/apps/icons/vaiz_1775067180548.png" alt="Vaiz logo" width="28" height="28"> Vaiz: Universal API

Project management workspace for boards, tasks, milestones, documents, comments, members, and related planning data in Vaiz.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/vaiz/latest
- **Category:** Productivity / Project Management
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://vaiz.com
- **Vendor API docs:** https://docs-python-sdk.vaiz.com/api-reference/overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Profile](actions/get-profile.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vaiz/latest/actions/get-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Boards

| Action | Method | Description |
| --- | --- | --- |
| [Get Board](actions/get-board.md) | GET | Retrieves a board record from Vaiz. |
| [List Boards](actions/list-boards.md) | GET | Retrieves all board records from Vaiz. |

### Comments

| Action | Method | Description |
| --- | --- | --- |
| [Create Comment](actions/create-comment.md) | POST | Creates a new comment in Vaiz. |
| [Delete Comment](actions/delete-comment.md) | DELETE | Deletes an existing comment from Vaiz. |
| [List Comments](actions/list-comments.md) | GET | Retrieves all comment records from Vaiz. |
| [Update Comment](actions/update-comment.md) | PUT | Updates an existing comment in Vaiz. |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Append Document](actions/append-document.md) | PUT | Appends content to an existing document in Vaiz. |
| [Append JSON Document](actions/append-json-document.md) | PUT | Appends JSON content to an existing document in Vaiz. |
| [Create Document](actions/create-document.md) | POST | Creates a new document in Vaiz. |
| [Get JSON Document](actions/get-json-document.md) | GET | Retrieves a document structure in JSON from Vaiz. |
| [List Documents](actions/list-documents.md) | GET | Retrieves all document records from Vaiz. |
| [Replace Document](actions/replace-document.md) | PUT | Replaces existing document content in Vaiz. |
| [Replace JSON Document](actions/replace-json-document.md) | PUT | Replaces a JSON document structure in Vaiz. |
| [Update Document](actions/update-document.md) | PUT | Updates an existing document in Vaiz. |

### Milestones

| Action | Method | Description |
| --- | --- | --- |
| [Create Milestone](actions/create-milestone.md) | POST | Creates a new milestone in Vaiz. |
| [Get Milestone](actions/get-milestone.md) | GET | Retrieves a milestone record from Vaiz. |
| [List Milestones](actions/list-milestones.md) | GET | Retrieves all milestone records from Vaiz. |
| [Toggle Milestone](actions/toggle-milestone.md) | PUT | Updates a milestone status in Vaiz. |
| [Update Milestone](actions/update-milestone.md) | PUT | Updates an existing milestone in Vaiz. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Get Project](actions/get-project.md) | GET | Retrieves a project record from Vaiz. |
| [List Projects](actions/list-projects.md) | GET | Retrieves all project records from Vaiz. |

### Reactions

| Action | Method | Description |
| --- | --- | --- |
| [Add Reaction](actions/add-reaction.md) | POST | Adds a reaction to a comment in Vaiz. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST | Creates a new task in Vaiz. |
| [Get Task](actions/get-task.md) | GET | Retrieves a task record from Vaiz. |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves all task records from Vaiz. |
| [Move Tasks](actions/move-tasks.md) | PUT | Moves existing tasks between stages in Vaiz. |
| [Update Task](actions/update-task.md) | PUT | Updates an existing task in Vaiz. |

### User Profiles

| Action | Method | Description |
| --- | --- | --- |
| [Get Profile](actions/get-profile.md) | GET | Retrieves the authenticated user profile from Vaiz. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [List Space Members](actions/list-space-members.md) | GET | Retrieves all members in a Vaiz space. |

### Workspaces

| Action | Method | Description |
| --- | --- | --- |
| [Get Space](actions/get-space.md) | GET | Retrieves the current space from Vaiz. |

