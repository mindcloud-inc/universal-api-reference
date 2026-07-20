# <img src="https://images.mindcloud.co/apps/icons/humanitix_1773411652680.png" alt="Humanitix logo" width="28" height="28"> Humanitix: Universal API

The Humanitix Public API for fetching event, order, ticket, or tag information.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/humanitix/latest
- **Category:** Support / Ticketing
- **Actions:** 4
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://humanitix.com
- **Vendor API docs:** https://humanitix.stoplight.io/docs/humanitix-public-api/e508a657c1467-humanitix-public-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Events](actions/list-events.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/humanitix/latest/actions/list-events?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (4)

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Get Event](actions/get-event.md) | GET | Retrieves an event from Humanitix by event ID. |
| [List Events](actions/list-events.md) | GET | Retrieves events from Humanitix for the connected account. |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Get Order](actions/get-order.md) | GET | Retrieves an order for an event from Humanitix. |
| [List Orders](actions/list-orders.md) | GET | Retrieves orders for an event from Humanitix. |

