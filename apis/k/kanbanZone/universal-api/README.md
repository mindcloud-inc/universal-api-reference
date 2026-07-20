# <img src="https://images.mindcloud.co/apps/icons/kanban-zone_1774887509944.png" alt="Kanban Zone logo" width="28" height="28"> Kanban Zone: Universal API

Manage Kanban boards, cards, comments, metrics, and webhooks

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/kanbanZone/latest
- **Category:** Productivity / Project Management
- **Actions:** 23
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://kanbanzone.com
- **Vendor API docs:** https://docs.kanbanzone.io/apiReference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Boards](actions/list-boards.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kanbanZone/latest/actions/list-boards?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (23)

### Boards

| Action | Method | Description |
| --- | --- | --- |
| [Get Board](actions/get-board.md) | GET | Retrieves a board from Kanban Zone. |
| [List Boards](actions/list-boards.md) | GET | Retrieves boards from Kanban Zone. |

### Card

| Action | Method | Description |
| --- | --- | --- |
| [Add Cards](actions/add-cards.md) | POST | Creates cards in Kanban Zone. |
| [Get Card](actions/get-card.md) | GET | Retrieves a card from Kanban Zone. |
| [List Cards](actions/list-cards.md) | GET | Retrieves cards from Kanban Zone. |
| [Move Card](actions/move-card.md) | PUT | Moves a card in Kanban Zone. |
| [Update Card](actions/update-card.md) | PUT | Updates an existing card in Kanban Zone. |

### Comments

| Action | Method | Description |
| --- | --- | --- |
| [Create Card Comment](actions/create-card-comment.md) | POST | Creates a card comment in Kanban Zone. |
| [List Card Comments](actions/list-card-comments.md) | GET | Retrieves comments for a Kanban Zone card. |

### Metrics

| Action | Method | Description |
| --- | --- | --- |
| [Get Card Metrics](actions/get-card-metrics.md) | GET | Retrieves metrics for a Kanban Zone card. |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Get Abandoned Effort Report](actions/get-abandoned-effort-report.md) | GET | Retrieves an abandoned effort report from Kanban Zone. |
| [Get Allocation Report](actions/get-allocation-report.md) | GET | Retrieves an allocation report from Kanban Zone. |
| [Get Arrival Rate Report](actions/get-arrival-rate-report.md) | GET | Retrieves an arrival rate report from Kanban Zone. |
| [Get Cycle Time Report](actions/get-cycle-time-report.md) | GET | Retrieves a cycle time report from Kanban Zone. |
| [Get Flow Efficiency Report](actions/get-flow-efficiency-report.md) | GET | Retrieves a flow efficiency report from Kanban Zone. |
| [Get Flow Report](actions/get-flow-report.md) | GET | Retrieves a flow report from Kanban Zone. |
| [Get Lead Time Report](actions/get-lead-time-report.md) | GET | Retrieves a lead time report from Kanban Zone. |
| [Get Throughput Report](actions/get-throughput-report.md) | GET | Retrieves a throughput report from Kanban Zone. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a webhook in Kanban Zone. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes an existing webhook from Kanban Zone. |
| [Get Webhook Details](actions/get-webhook-details.md) | GET | Retrieves a webhook from Kanban Zone. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks from Kanban Zone. |
| [Update Webhook](actions/update-webhook.md) | PUT | Updates an existing webhook in Kanban Zone. |

