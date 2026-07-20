# Lulu: Create Print Job Cost Calculation

Calculates print job costs in Lulu.

```
GET https://connect.mindcloud.co/v1/universal/lulu/latest/actions/create-print-job-cost-calculation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lulu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lulu/latest/actions/create-print-job-cost-calculation?connectionId=$CONNECTION_ID&lineItems%5B%5D=%5Bobject%20Object%5D&shippingAddress=%5Bobject%20Object%5D&shippingOption=MAIL" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "lineItems[]": "[object Object]",
  "shippingAddress": "[object Object]",
  "shippingOption": "MAIL"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lulu/latest/actions/create-print-job-cost-calculation?${params}`, {
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
| `lineItems[]` | array | yes | Array of Lulu line items to price. Default: `[{"quantity":1,"page_count":32,"pod_package_id":"0600X0900.BW.STD.PB.060UW444.MXX"}]`. |
| `shippingAddress` | object | yes | Shipping address used for Lulu cost calculation. Default: `{"city":"Washington","street1":"101 Independence Ave SE","postcode":"20540","state_code":"DC","country_code":"US","phone_number":"+12025550123"}`. |
| `shippingOption` | string | yes | Lulu shipping option level. Default: `MAIL`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "currency": "string",
      "lineItemCosts": [
        [
          {}
        ]
      ],
      "shippingAddress": {
        "city": "string",
        "countryCode": "string"
      },
      "shippingCost": {
        "totalCostExclTax": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currency` | string |  |
| `lineItemCosts[]` | array<object> |  |
| `lineItemCosts[].costExclDiscounts` | string |  |
| `lineItemCosts[].discounts[]` | array<object> |  |
| `lineItemCosts[].quantity` | number |  |
| `shippingAddress` | object |  |
| `shippingAddress.city` | string |  |
| `shippingAddress.countryCode` | string |  |
| `shippingCost` | object |  |
| `shippingCost.totalCostExclTax` | string |  |

## Native endpoint

Through the native Lulu API, this operation is `POST /print-job-cost-calculations/` (base URL `{{credentials.apiBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-print-job-cost-calculation.md) for the provider-specific parameters and requirements.

