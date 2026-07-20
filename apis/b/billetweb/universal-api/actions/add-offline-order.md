# Billetweb: Add Offline Order

Creates a new offline order in Billetweb.

```
POST https://connect.mindcloud.co/v1/universal/billetweb/latest/actions/add-offline-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Billetweb `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/billetweb/latest/actions/add-offline-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "data[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/billetweb/latest/actions/add-offline-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "data[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Event identifier that will receive offline orders. |
| `data[]` | array<object> | yes | Array of offline order objects to add. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Billetweb API returns.

## Native endpoint

Through the native Billetweb API, this operation is `POST /event/:id/add_order` (base URL `https://www.billetweb.fr/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-offline-order.md) for the provider-specific parameters and requirements.

