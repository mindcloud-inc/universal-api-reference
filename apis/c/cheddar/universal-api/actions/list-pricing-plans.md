# Cheddar: List Pricing Plans

Retrieves pricing plan records from Cheddar.

```
GET https://connect.mindcloud.co/v1/universal/cheddar/latest/actions/list-pricing-plans
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cheddar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cheddar/latest/actions/list-pricing-plans?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cheddar/latest/actions/list-pricing-plans?${params}`, {
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
      "plans": [
        {
          "billingFrequency": "string",
          "billingFrequencyQuantity": 1,
          "code": "string",
          "createdDatetime": "2026-05-07T12:00:00.000Z",
          "description": "string",
          "id": "string",
          "isActive": true,
          "isFree": true,
          "items": [
            {
              "code": "string",
              "createdDatetime": "2026-05-07T12:00:00.000Z",
              "id": "string",
              "isPeriodic": true,
              "name": "Ava Chen",
              "overageAmount": 1,
              "quantityIncluded": 1
            }
          ],
          "name": "Ava Chen",
          "recurringChargeAmount": 1,
          "recurringChargeCode": "string",
          "setupChargeAmount": 1,
          "setupChargeCode": "string",
          "trialDays": 1
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `plans` | array<object> |  |
| `plans[].billingFrequency` | string |  |
| `plans[].billingFrequencyQuantity` | number |  |
| `plans[].code` | string |  |
| `plans[].createdDatetime` | date |  |
| `plans[].description` | string |  |
| `plans[].id` | string |  |
| `plans[].isActive` | boolean |  |
| `plans[].isFree` | boolean |  |
| `plans[].items` | array<object> |  |
| `plans[].items[].code` | string |  |
| `plans[].items[].createdDatetime` | date |  |
| `plans[].items[].id` | string |  |
| `plans[].items[].isPeriodic` | boolean |  |
| `plans[].items[].name` | string |  |
| `plans[].items[].overageAmount` | number |  |
| `plans[].items[].quantityIncluded` | number |  |
| `plans[].name` | string |  |
| `plans[].recurringChargeAmount` | number |  |
| `plans[].recurringChargeCode` | string |  |
| `plans[].setupChargeAmount` | number |  |
| `plans[].setupChargeCode` | string |  |
| `plans[].trialDays` | number |  |

## Native endpoint

Through the native Cheddar API, this operation is `GET /plans/get/productCode/{{credentials.productCode}}` (base URL `https://getcheddar.com/xml`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-pricing-plans.md) for the provider-specific parameters and requirements.

