# HubSpot: Batch Create Orders

Creates new orders in HubSpot in a batch.

```
POST https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/batch-create-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HubSpot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/batch-create-orders" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "inputs[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/batch-create-orders', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "inputs[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `inputs[]` | array<object> | yes | Array of order objects to create (HubSpot batch create payload). |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native HubSpot API returns.

## Native endpoint

Through the native HubSpot API, this operation is `POST crm/v3/objects/orders/batch/create` (base URL `https://api.hubapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/batch-create-orders.md) for the provider-specific parameters and requirements.

