# <img src="https://images.mindcloud.co/apps/icons/hipsy_1774376978389.png" alt="Hipsy logo" width="28" height="28"> Hipsy: Universal API

Manage Hipsy organisations, events, and ticket orders

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/hipsy/latest
- **Category:** Marketing / Events & Webinars
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://hipsy.nl
- **Vendor API docs:** https://docs.hipsy.nl/api-reference/getting-started

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Organisations](actions/list-organisations.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hipsy/latest/actions/list-organisations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Event

| Action | Method | Description |
| --- | --- | --- |
| [List Events](actions/list-events.md) | GET | Retrieves events from a Hipsy organisation. |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [List Orders](actions/list-orders.md) | GET | Retrieves orders from a Hipsy organisation. |

### Organisation

| Action | Method | Description |
| --- | --- | --- |
| [List Organisations](actions/list-organisations.md) | GET | Retrieves organisations from Hipsy. |

