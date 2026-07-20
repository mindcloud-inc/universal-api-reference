# <img src="https://images.mindcloud.co/apps/icons/image-2827-vectorized_1777380907309.png" alt="Trello logo" width="28" height="28"> Trello: Universal API

Organize work with boards, track cards, manage tasks, and collaborate.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/trello/latest
- **Category:** Support / Ticketing
- **Actions:** 32
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://trello.com/
- **Vendor API docs:** https://developer.atlassian.com/cloud/trello/rest/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Member](actions/get-member.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trello/latest/actions/get-member?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (32)

### Collections

| Action | Method | Description |
| --- | --- | --- |
| [Add CheckItem to Checklist](actions/add-check-item-to-checklist.md) | POST | Creates a check item in a Trello checklist. |
| [Archive Board](actions/archive-board.md) | PUT | Archives an existing board in Trello. |
| [Archive List](actions/archive-list.md) | PUT | Archives an existing list in Trello. |
| [Create Board](actions/create-board.md) | POST | Creates a new board in Trello. |
| [Create Checklist](actions/create-checklist.md) | POST | Creates a new checklist in Trello. |
| [Create List on Board](actions/create-list-on-board.md) | POST | Creates a new list on a Trello board. |
| [Delete CheckItem from Checklist](actions/delete-check-item-from-checklist.md) | DELETE | Deletes a check item from a Trello checklist. |
| [Get Actions on a Card](actions/get-actions-on-a-card.md) | GET | Retrieves actions on a card from Trello. |
| [Get Attachments on a Card](actions/get-attachments-on-a-card.md) | GET | Retrieves attachments on a card from Trello. |
| [Get Board](actions/get-board.md) | GET | Retrieves a board from Trello. |
| [Get Cards in a List](actions/get-cards-in-a-list.md) | GET | Retrieves cards in a list from Trello. |
| [Get Checklists on a Card](actions/get-checklists-on-a-card.md) | GET | Retrieves checklists on a card from Trello. |
| [Get List](actions/get-list.md) | GET | Retrieves a list from Trello. |
| [Get Lists on a Board](actions/get-lists-on-a-board.md) | GET | Retrieves lists on a board from Trello. |
| [List Boards By Member](actions/list-boards-by-member.md) | GET | Retrieves boards for a member from Trello. |
| [Search Trello](actions/search-trello.md) | GET | Finds boards, cards, or members in Trello. |
| [Update Board](actions/update-board.md) | PUT | Updates an existing board in Trello. |
| [Update List](actions/update-list.md) | PUT | Updates an existing list in Trello. |

### Tickets

| Action | Method | Description |
| --- | --- | --- |
| [Add Attachment to Card](actions/add-attachment-to-card.md) | PUT | Adds an attachment to a Trello card. |
| [Add Comment to Card](actions/add-comment-to-card.md) | POST | Creates a comment on a Trello card. |
| [Add Label to Card](actions/add-label-to-card.md) | PUT | Adds a label to a Trello card. |
| [Add Member to Card](actions/add-member-to-card.md) | PUT | Adds a member to a Trello card. |
| [Create Card](actions/create-card.md) | POST | Creates a new card in Trello. |
| [Create Checklist on a Card](actions/create-checklist-on-a-card.md) | POST | Creates a checklist on a Trello card. |
| [Delete Attachment from Card](actions/delete-attachment-from-card.md) | DELETE | Deletes an attachment from a Trello card. |
| [Delete Card](actions/delete-card.md) | DELETE | Deletes an existing card from Trello. |
| [Get Card](actions/get-card.md) | GET | Retrieves a card from Trello. |
| [Get Cards on a Board](actions/get-cards-on-a-board.md) | GET | Retrieves cards on a board from Trello. |
| [Remove Label from Card](actions/remove-label-from-card.md) | DELETE | Removes a label from a Trello card. |
| [Remove Member from Card](actions/remove-member-from-card.md) | DELETE | Removes a member from a Trello card. |
| [Update Card](actions/update-card.md) | PUT | Updates an existing card in Trello. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Member](actions/get-member.md) | GET | Retrieves a member from Trello. |

