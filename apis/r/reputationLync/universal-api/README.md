# <img src="https://images.mindcloud.co/apps/icons/tmp5fs-qnwr_1774459675879.png" alt="ReputationLync logo" width="28" height="28"> ReputationLync: Universal API

Manage customers and automate review requests and feedback outreach

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/reputationLync/latest
- **Category:** Support / Customer Success
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.reputationlyncs.com
- **Vendor API docs:** https://documenter.getpostman.com/view/25361963/2s93Xzw2bS

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Validate API Key](actions/validate-api-key.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reputationLync/latest/actions/validate-api-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Api Key

| Action | Method | Description |
| --- | --- | --- |
| [Validate API Key](actions/validate-api-key.md) | GET | Validates an API key in ReputationLync. |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Add Customer](actions/add-customer.md) | POST | Creates a new customer in ReputationLync. |
| [List Customers](actions/list-customers.md) | GET | Retrieves customers from ReputationLync. |

