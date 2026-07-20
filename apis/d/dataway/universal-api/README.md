# <img src="https://images.mindcloud.co/apps/icons/dataway_1776449922594.png" alt="Dataway logo" width="28" height="28"> Dataway: Universal API

Dataway vendor API for service discovery, balance checks, biller validation, vending, and transaction lookup using vendor keys.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/dataway/latest
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://datawayapp.com
- **Vendor API docs:** https://documenter.getpostman.com/view/421216/UV5Ukz4U

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Balance](actions/get-balance.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataway/latest/actions/get-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Category

| Action | Method | Description |
| --- | --- | --- |
| [List Service Categories](actions/list-service-categories.md) | GET | Retrieves available service categories from Dataway. |

### Ledger Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Balance](actions/get-balance.md) | GET | Retrieves the current vendor balance from Dataway. |

### Service

| Action | Method | Description |
| --- | --- | --- |
| [List Service Variations](actions/list-service-variations.md) | GET | Retrieves service variations from Dataway for a selected service. |
| [List Services](actions/list-services.md) | GET | Retrieves available services from Dataway for a selected category. |

### Service Request

| Action | Method | Description |
| --- | --- | --- |
| [Validate Biller](actions/validate-biller.md) | GET | Validates a biller in Dataway for a selected service. |

### Transaction

| Action | Method | Description |
| --- | --- | --- |
| [Query Transaction](actions/query-transaction.md) | GET | Retrieves transaction details from Dataway by client reference. |
| [Vend Service](actions/vend-service.md) | POST | Creates a new vend transaction in Dataway. |

