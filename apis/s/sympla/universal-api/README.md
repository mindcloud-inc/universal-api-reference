# <img src="https://images.mindcloud.co/apps/icons/images_1773936192812.png" alt="Sympla logo" width="28" height="28"> Sympla: Universal API

Access Sympla organizer data including events, orders, participants, check-ins, and affiliates via the public organizer API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sympla/latest
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.sympla.com.br/
- **Vendor API docs:** https://developers.sympla.com.br/api-doc/index.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Events](actions/list-events.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sympla/latest/actions/list-events?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Get Event By ID](actions/get-event-by-id.md) | GET | Retrieves an event from Sympla by event ID. |
| [List Events](actions/list-events.md) | GET | Retrieves the organizer's events from Sympla. |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Get Order By ID](actions/get-order-by-id.md) | GET | Retrieves an order from Sympla by order ID. |
| [List Orders By Event](actions/list-orders-by-event.md) | GET | Retrieves orders from Sympla for a specific event. |

### Participant

| Action | Method | Description |
| --- | --- | --- |
| [Check In Participant](actions/check-in-participant.md) | PUT | Checks in a participant in Sympla by participant ID. |
| [List Participants By Event](actions/list-participants-by-event.md) | GET | Retrieves participants from Sympla for a specific event. |
| [List Participants By Order](actions/list-participants-by-order.md) | GET | Retrieves participants from Sympla for a specific order. |

