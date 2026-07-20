# <img src="https://images.mindcloud.co/apps/icons/peggy-pay_1776870184954.png" alt="Peggy Pay logo" width="28" height="28"> Peggy Pay: Universal API

Manage Peggy Pay submissions, orders, and webhook-backed checkout data

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/peggyPay/latest
- **Category:** Commerce / Payments & Billing
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.peggypay.com
- **Vendor API docs:** https://www.peggypay.com/kennisbank

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Authorize API Key](actions/authorize-api-key.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/peggyPay/latest/actions/authorize-api-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (5)

### Access Tokens

| Action | Method | Description |
| --- | --- | --- |
| [Authorize API Key](actions/authorize-api-key.md) | GET | Retrieves an access token from Peggy Pay. |

### Form Submissions

| Action | Method | Description |
| --- | --- | --- |
| [Add Submission Item](actions/add-submission-item.md) | PUT | Updates a Peggy Pay submission by adding an item. |
| [Get Submission by Hash](actions/get-submission-by-hash.md) | GET | Retrieves a submission from Peggy Pay by submission hash. |

### Orders

| Action | Method | Description |
| --- | --- | --- |
| [Get Order by Order Hash](actions/get-order-by-order-hash.md) | GET | Retrieves an order from Peggy Pay by order hash. |
| [Get Order by Submission Hash](actions/get-order-by-submission-hash.md) | GET | Retrieves an order from Peggy Pay by submission hash. |

