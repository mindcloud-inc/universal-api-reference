# <img src="https://images.mindcloud.co/apps/icons/teamhood_1774644205617.png" alt="Teamhood logo" width="28" height="28"> Teamhood: Universal API

Manage Teamhood workspaces, boards, rows, items, attachments, users, logs, and timelogs through the Teamhood REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/teamhood/latest
- **Category:** Support / Ticketing
- **Actions:** 19
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://teamhood.com
- **Vendor API docs:** https://api-mindcloud1.teamhood.com/swagger/index.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Workspaces](actions/list-workspaces.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teamhood/latest/actions/list-workspaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (19)

### Attachments

| Action | Method | Description |
| --- | --- | --- |
| [Delete Attachment](actions/delete-attachment.md) | DELETE | Deletes an attachment from Teamhood. |
| [Download Attachment Content](actions/download-attachment-content.md) | GET | Downloads uploaded attachment content from Teamhood. |
| [Get Attachment](actions/get-attachment.md) | GET | Retrieves attachment metadata from Teamhood by ID. |
| [List Item Attachments](actions/list-item-attachments.md) | GET | Retrieves attachments for a Teamhood item. |

### Board

| Action | Method | Description |
| --- | --- | --- |
| [List Workspace Boards](actions/list-workspace-boards.md) | GET | Retrieves boards for a Teamhood workspace. |

### Boards

| Action | Method | Description |
| --- | --- | --- |
| [List Board Rows](actions/list-board-rows.md) | GET | Retrieves rows for a Teamhood board. |
| [List Board Templates](actions/list-board-templates.md) | GET | Retrieves available board templates from Teamhood. |

### Item

| Action | Method | Description |
| --- | --- | --- |
| [Query Items](actions/query-items.md) | GET | Finds items in Teamhood by query filters. |

### Items

| Action | Method | Description |
| --- | --- | --- |
| [Create Item](actions/create-item.md) | POST | Creates a new item in Teamhood. |
| [Delete Item](actions/delete-item.md) | DELETE | Deletes an existing item from Teamhood. |
| [Get Item](actions/get-item.md) | GET | Retrieves item details from Teamhood by ID. |
| [List Item Activities](actions/list-item-activities.md) | GET | Retrieves Teamhood item activities for a board and time range. |
| [List Timelogs](actions/list-timelogs.md) | GET | Retrieves timelogs from Teamhood by request filters. |
| [Update Item](actions/update-item.md) | PUT | Updates an existing item in Teamhood. |

### Status

| Action | Method | Description |
| --- | --- | --- |
| [List Board Statuses](actions/list-board-statuses.md) | GET | Retrieves statuses for a Teamhood board. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [List Users](actions/list-users.md) | GET | Retrieves all available users from Teamhood. |

### Workspace

| Action | Method | Description |
| --- | --- | --- |
| [Get Workspace](actions/get-workspace.md) | GET | Retrieves workspace details from Teamhood by ID. |
| [List Workspaces](actions/list-workspaces.md) | GET | Retrieves all accessible workspaces from Teamhood. |

### Workspaces

| Action | Method | Description |
| --- | --- | --- |
| [List Workspace Templates](actions/list-workspace-templates.md) | GET | Retrieves available workspace templates from Teamhood. |

