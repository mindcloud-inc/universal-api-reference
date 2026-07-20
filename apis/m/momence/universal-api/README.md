# <img src="https://images.mindcloud.co/apps/icons/momence-brandmark-blue_1776107995709.png" alt="Momence logo" width="28" height="28"> Momence: Universal API

Momence legacy host-scoped API token app for the verified v1 surface at https://momence.com/_api/primary/api/v1.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/momence/latest
- **Category:** Productivity / Scheduling
- **Actions:** 4
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://momence.com
- **Vendor API docs:** https://api.docs.momence.com

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Events](actions/list-events.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/momence/latest/actions/list-events?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (4)

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [List Customers](actions/list-customers.md) | GET |  |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [List Events](actions/list-events.md) | GET |  |

### Membership

| Action | Method | Description |
| --- | --- | --- |
| [List Memberships](actions/list-memberships.md) | GET |  |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [List Products](actions/list-products.md) | GET |  |

