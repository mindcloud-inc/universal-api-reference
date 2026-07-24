# Cin7 Core: Update Sale Fulfillment Pack



```
PUT https://connect.mindcloud.co/v1/universal/cin7core/latest/actions/update-sale-fulfillment-pack
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cin7 Core `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/cin7core/latest/actions/update-sale-fulfillment-pack" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "TaskID": "string",
  "Status": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cin7core/latest/actions/update-sale-fulfillment-pack', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "TaskID": "string",
    "Status": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `Lines[].ProductID` | string | no |  |
| `TaskID` | string | yes |  |
| `Lines[].SKU` | string | no |  |
| `Status` | string | yes |  |
| `Lines[]` | array<object> | no |  |
| `Lines[].Name` | string | no |  |
| `Lines[].Location` | string | no |  |
| `Lines[].LocationID` | string | no |  |
| `Lines[].Box` | string | no |  |
| `Lines[].Quantity` | number | no |  |
| `Lines[].BatchSN` | string | no |  |
| `Lines[].ExpiryDate` | string | no |  |
| `Lines[].WarrantyRegistrationNumber` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Cin7 Core API returns.

## Native endpoint

Through the native Cin7 Core API, this operation is `PUT sale/fulfilment/pack` (base URL `https://inventory.dearsystems.com/externalapi/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-sale-fulfillment-pack.md) for the provider-specific parameters and requirements.

