# Cin7 Core: Create Sale Fulfillment Pick



```
POST https://connect.mindcloud.co/v1/universal/cin7core/latest/actions/create-sale-fulfillment-pick
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cin7 Core `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cin7core/latest/actions/create-sale-fulfillment-pick" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "status": "string",
  "taskID": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cin7core/latest/actions/create-sale-fulfillment-pick', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "status": "string",
    "taskID": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `lines[].productID` | string | no |  |
| `lines[].sKU` | string | no |  |
| `lines[].name` | string | no |  |
| `lines[].location` | string | no |  |
| `lines[].locationID` | string | no |  |
| `lines[].quantity` | number | no |  |
| `lines[].batchSN` | string | no |  |
| `lines[].expiryDate` | string | no |  |
| `lines[]` | array<object> | no |  |
| `status` | string | yes |  |
| `taskID` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Cin7 Core API returns.

## Native endpoint

Through the native Cin7 Core API, this operation is `POST sale/fulfilment/pick` (base URL `https://inventory.dearsystems.com/externalapi/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-sale-fulfillment-pick.md) for the provider-specific parameters and requirements.

