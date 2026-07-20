# retailCRM: List Delivery Types

Retrieves delivery types from retailCRM.

```
GET https://connect.mindcloud.co/v1/universal/retailCRM/latest/actions/list-delivery-types
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a retailCRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/retailCRM/latest/actions/list-delivery-types?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/retailCRM/latest/actions/list-delivery-types?${params}`, {
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
      "active": true,
      "code": "string",
      "currency": "string",
      "defaultCost": 1,
      "defaultForCrm": true,
      "defaultNetCost": 1,
      "deliveryPaymentTypes": [
        {
          "cod": true,
          "code": "string"
        }
      ],
      "deliveryServices": [
        "string"
      ],
      "isAutoCostCalculation": true,
      "isAutoNetCostCalculation": true,
      "isCostDependsOnDateTime": true,
      "isCostDependsOnRegionAndWeightAndSum": true,
      "isDynamicCostCalculation": true,
      "name": "Ava Chen",
      "paymentTypes": [
        "string"
      ],
      "sites": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `code` | string |  |
| `currency` | string |  |
| `defaultCost` | number |  |
| `defaultForCrm` | boolean |  |
| `defaultNetCost` | number |  |
| `deliveryPaymentTypes[].cod` | boolean |  |
| `deliveryPaymentTypes[].code` | string |  |
| `deliveryServices` | array |  |
| `isAutoCostCalculation` | boolean |  |
| `isAutoNetCostCalculation` | boolean |  |
| `isCostDependsOnDateTime` | boolean |  |
| `isCostDependsOnRegionAndWeightAndSum` | boolean |  |
| `isDynamicCostCalculation` | boolean |  |
| `name` | string |  |
| `paymentTypes[]` | string |  |
| `sites` | array |  |

## Native endpoint

Through the native retailCRM API, this operation is `GET /reference/delivery-types` (base URL `{{credentials.accountUrl}}/api/v5`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-delivery-types.md) for the provider-specific parameters and requirements.

