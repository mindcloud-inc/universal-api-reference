# Lulu: Get Print Job Costs

Retrieves costs for a print job from Lulu.

```
GET https://connect.mindcloud.co/v1/universal/lulu/latest/actions/get-print-job-costs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lulu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lulu/latest/actions/get-print-job-costs?connectionId=$CONNECTION_ID&id=job_123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "job_123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lulu/latest/actions/get-print-job-costs?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Lulu print job ID. Default: `job_123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "currency": "string",
      "fulfillmentCost": {},
      "lineItemCosts": [
        [
          {}
        ]
      ],
      "shippingCost": {},
      "totalCostExclTax": "string",
      "totalCostInclTax": "string",
      "totalDiscountAmount": "string",
      "totalTax": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currency` | string |  |
| `fulfillmentCost` | object |  |
| `lineItemCosts[]` | array<object> |  |
| `lineItemCosts[].lineItemExternalId` | string |  |
| `lineItemCosts[].lineItemId` | number |  |
| `shippingCost` | object |  |
| `totalCostExclTax` | string |  |
| `totalCostInclTax` | string |  |
| `totalDiscountAmount` | string |  |
| `totalTax` | string |  |

## Native endpoint

Through the native Lulu API, this operation is `GET /print-jobs/{id}/costs/` (base URL `{{credentials.apiBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-print-job-costs.md) for the provider-specific parameters and requirements.

