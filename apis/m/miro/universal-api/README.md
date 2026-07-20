# <img src="https://images.mindcloud.co/apps/icons/miro_1772994911645.png" alt="Miro logo" width="28" height="28"> Miro: Universal API

Brainstorm ideas, run workshops, map processes, and collaborate visually.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/miro/latest
- **Category:** Productivity / Project Management
- **Actions:** 25
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://miro.com
- **Vendor API docs:** https://developers.miro.com/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Access Token Context](actions/get-access-token-context.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/miro/latest/actions/get-access-token-context?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (25)

### Access Token

| Action | Method | Description |
| --- | --- | --- |
| [Get Access Token Context](actions/get-access-token-context.md) | GET | Retrieves access token context from Miro. |

### Board

| Action | Method | Description |
| --- | --- | --- |
| [Create Board](actions/create-board.md) | POST | Creates a new board in Miro. |
| [Delete Board](actions/delete-board.md) | DELETE | Deletes an existing board from Miro. |
| [Get Board](actions/get-board.md) | GET | Retrieves a board from Miro. |
| [List Boards](actions/list-boards.md) | GET | Retrieves boards from Miro. |
| [Update Board](actions/update-board.md) | PUT | Updates an existing board in Miro. |

### Item

| Action | Method | Description |
| --- | --- | --- |
| [List Items](actions/list-items.md) | GET | Retrieves items from a Miro board. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Create Card](actions/create-card.md) | POST | Creates a new card in Miro. |
| [Create Sticky Note](actions/create-sticky-note.md) | POST | Creates a new sticky note in Miro. |
| [Create Text](actions/create-text.md) | POST | Creates a new text item in Miro. |
| [Delete Card](actions/delete-card.md) | DELETE | Deletes an existing card from Miro. |
| [Delete Item](actions/delete-item.md) | DELETE | Deletes an item from a Miro board. |
| [Delete Sticky Note](actions/delete-sticky-note.md) | DELETE | Deletes an existing sticky note from Miro. |
| [Delete Text](actions/delete-text.md) | DELETE | Deletes an existing text item from Miro. |
| [Get Card](actions/get-card.md) | GET | Retrieves a card from Miro. |
| [Get Item](actions/get-item.md) | GET | Retrieves an item from a Miro board. |
| [Get Sticky Note](actions/get-sticky-note.md) | GET | Retrieves a sticky note from Miro. |
| [Get Text](actions/get-text.md) | GET | Retrieves a text item from Miro. |
| [List Board Members](actions/list-board-members.md) | GET | Retrieves board members from Miro. |
| [Remove Board Member](actions/remove-board-member.md) | DELETE | Removes a board member from Miro. |
| [Share Board](actions/share-board.md) | POST | Shares a board with a member in Miro. |
| [Update Card](actions/update-card.md) | PUT | Updates an existing card in Miro. |
| [Update Item Position](actions/update-item-position.md) | PUT | Updates an item's position or parent in Miro. |
| [Update Sticky Note](actions/update-sticky-note.md) | PUT | Updates an existing sticky note in Miro. |
| [Update Text](actions/update-text.md) | PUT | Updates an existing text item in Miro. |

