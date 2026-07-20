# <img src="https://images.mindcloud.co/apps/icons/placker_1775491365351.png" alt="Placker logo" width="28" height="28"> Placker: Universal API

Manage boards, cards, timelines, and reports across projects

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/placker/latest
- **Category:** Productivity / Project Management
- **Actions:** 33
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://placker.com/
- **Vendor API docs:** https://placker.com/docs/api/index.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List User Notifications](actions/list-user-notifications.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/placker/latest/actions/list-user-notifications?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (33)

### Board

| Action | Method | Description |
| --- | --- | --- |
| [Get Board Details](actions/get-board-details.md) | GET |  |
| [List Boards](actions/list-boards.md) | GET |  |

### Board Attribute

| Action | Method | Description |
| --- | --- | --- |
| [List Board Attributes](actions/list-board-attributes.md) | GET |  |

### Board Label

| Action | Method | Description |
| --- | --- | --- |
| [List Board Labels](actions/list-board-labels.md) | GET |  |

### Board Member

| Action | Method | Description |
| --- | --- | --- |
| [List Board Members](actions/list-board-members.md) | GET |  |

### Card

| Action | Method | Description |
| --- | --- | --- |
| [Create Card On List](actions/create-card-on-list.md) | POST |  |
| [Get Card Details](actions/get-card-details.md) | GET |  |
| [List Cards On Board](actions/list-cards-on-board.md) | GET |  |
| [List Cards On List](actions/list-cards-on-list.md) | GET |  |
| [Mirror Card To Card](actions/mirror-card-to-card.md) | POST |  |
| [Mirror Checklist Item To Card](actions/mirror-checklist-item-to-card.md) | POST |  |
| [Search Cards](actions/search-cards.md) | GET |  |
| [Update Card](actions/update-card.md) | PUT |  |

### Card Comment

| Action | Method | Description |
| --- | --- | --- |
| [Add Card Comment](actions/add-card-comment.md) | POST |  |
| [List Card Comments](actions/list-card-comments.md) | GET |  |

### Card Label

| Action | Method | Description |
| --- | --- | --- |
| [Add Card Label](actions/add-card-label.md) | POST |  |
| [Remove Card Label](actions/remove-card-label.md) | DELETE |  |

### Card Member

| Action | Method | Description |
| --- | --- | --- |
| [Add Card Member](actions/add-card-member.md) | POST |  |
| [Remove Card Member](actions/remove-card-member.md) | DELETE |  |

### Checklist

| Action | Method | Description |
| --- | --- | --- |
| [Create Checklist On Card](actions/create-checklist-on-card.md) | POST |  |
| [Delete Checklist](actions/delete-checklist.md) | DELETE |  |
| [Get Checklist Details](actions/get-checklist-details.md) | GET |  |
| [List Card Checklists](actions/list-card-checklists.md) | GET |  |
| [Update Checklist](actions/update-checklist.md) | PUT |  |

### Item

| Action | Method | Description |
| --- | --- | --- |
| [Create Checklist Item](actions/create-checklist-item.md) | POST |  |
| [Delete Checklist Item](actions/delete-checklist-item.md) | DELETE |  |
| [Mirror Card To Checklist Item](actions/mirror-card-to-checklist-item.md) | POST |  |
| [Update Checklist Item](actions/update-checklist-item.md) | PUT |  |

### List

| Action | Method | Description |
| --- | --- | --- |
| [List Lists On Board](actions/list-lists-on-board.md) | GET |  |

### User Notification

| Action | Method | Description |
| --- | --- | --- |
| [List User Notifications](actions/list-user-notifications.md) | GET |  |

### Webhook Endpoint

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST |  |
| [Delete Webhook](actions/delete-webhook.md) | DELETE |  |

### Webhook Event

| Action | Method | Description |
| --- | --- | --- |
| [Get Webhook Example Data](actions/get-webhook-example-data.md) | GET |  |

