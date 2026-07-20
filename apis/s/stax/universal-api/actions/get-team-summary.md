# Stax: Get Team Summary

Retrieves team summary statistics from Stax.

```
GET https://connect.mindcloud.co/v1/universal/stax/latest/actions/get-team-summary
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stax `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stax/latest/actions/get-team-summary?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stax/latest/actions/get-team-summary?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "cachedAt": "string",
      "customerCount": 1,
      "hasAch": true,
      "hasHostedPaymentsTransactions": true,
      "invoiceCount": 1,
      "rateType": "string",
      "scheduledInvoiceCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cachedAt` | string | Cache timestamp. |
| `customerCount` | number | Number of customers. |
| `hasAch` | boolean | Whether ACH is enabled. |
| `hasHostedPaymentsTransactions` | boolean | Whether hosted payments transactions exist. |
| `invoiceCount` | number | Number of invoices. |
| `rateType` | string | Gateway rate type. |
| `scheduledInvoiceCount` | number | Number of scheduled invoices. |

## Native endpoint

Through the native Stax API, this operation is `GET /query/statistics/teamSummary` (base URL `https://apiprod.fattlabs.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-team-summary.md) for the provider-specific parameters and requirements.

