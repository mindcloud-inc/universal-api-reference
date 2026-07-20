# <img src="https://images.mindcloud.co/apps/icons/flowfast-logo_1775156526190.png" alt="FlowFast logo" width="28" height="28"> FlowFast: Universal API

FlowFast is a kanban-first project and work management platform for boards, columns, lanes, cards, comments, files, tags, and documents.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/flowFast/latest
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.flowfast.io
- **Vendor API docs:** https://apps.flowfast.io

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Spaces](actions/list-spaces.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flowFast/latest/actions/list-spaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Boards

| Action | Method | Description |
| --- | --- | --- |
| [Create Board](actions/create-board.md) | POST | Creates a new board in FlowFast. |
| [Get Board](actions/get-board.md) | GET | Retrieves board details from FlowFast. |
| [List Space Boards](actions/list-space-boards.md) | GET | Retrieves boards from a space in FlowFast. |

### Columns

| Action | Method | Description |
| --- | --- | --- |
| [Create Column](actions/create-column.md) | POST | Creates a new column in FlowFast. |
| [Delete Column](actions/delete-column.md) | DELETE | Deletes an existing column from FlowFast. |
| [List Board Columns](actions/list-board-columns.md) | GET | Retrieves columns from a board in FlowFast. |
| [Update Column](actions/update-column.md) | PUT | Updates an existing column in FlowFast. |

### Comments

| Action | Method | Description |
| --- | --- | --- |
| [Create Card Comment](actions/create-card-comment.md) | POST | Creates a new comment on a card in FlowFast. |
| [List Card Comments](actions/list-card-comments.md) | GET | Retrieves comments from a card in FlowFast. |
| [Update Card Comment](actions/update-card-comment.md) | PUT | Updates an existing card comment in FlowFast. |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Create Document](actions/create-document.md) | POST | Creates a new document in FlowFast. |
| [Delete Document](actions/delete-document.md) | DELETE | Deletes an existing document from FlowFast. |
| [Get Document](actions/get-document.md) | GET | Retrieves document details from FlowFast. |
| [List Documents](actions/list-documents.md) | GET | Retrieves documents from FlowFast. |
| [Update Document](actions/update-document.md) | PUT | Updates an existing document in FlowFast. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [List Card Files](actions/list-card-files.md) | GET | Retrieves files from a card in FlowFast. |

### Stages

| Action | Method | Description |
| --- | --- | --- |
| [List Board Lanes](actions/list-board-lanes.md) | GET | Retrieves lanes from a board in FlowFast. |
| [Update Lane](actions/update-lane.md) | PUT | Updates an existing lane in FlowFast. |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [Create Tag](actions/create-tag.md) | POST | Creates a new tag in FlowFast. |
| [List Card Tags](actions/list-card-tags.md) | GET | Retrieves tags from a card in FlowFast. |
| [List Tags](actions/list-tags.md) | GET | Retrieves tags from FlowFast. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Create Card](actions/create-card.md) | POST | Creates a new card in FlowFast. |
| [Delete Card](actions/delete-card.md) | DELETE | Deletes an existing card from FlowFast. |
| [Get Card](actions/get-card.md) | GET | Retrieves card details from FlowFast. |
| [List Cards](actions/list-cards.md) | GET | Retrieves cards from FlowFast. |
| [List Space Cards](actions/list-space-cards.md) | GET | Retrieves cards from a space in FlowFast. |
| [Update Card](actions/update-card.md) | PUT | Updates an existing card in FlowFast. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [List Users](actions/list-users.md) | GET | Retrieves users from FlowFast. |

### Workspaces

| Action | Method | Description |
| --- | --- | --- |
| [Get Space](actions/get-space.md) | GET | Retrieves space details from FlowFast. |
| [List Spaces](actions/list-spaces.md) | GET | Retrieves spaces from FlowFast. |

