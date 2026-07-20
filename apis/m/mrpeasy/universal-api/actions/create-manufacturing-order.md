# MRPeasy: Create Manufacturing Order

Creates a new manufacturing order in MRPeasy.

```
POST https://connect.mindcloud.co/v1/universal/mrpeasy/latest/actions/create-manufacturing-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MRPeasy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mrpeasy/latest/actions/create-manufacturing-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "articleId": 1,
  "quantity": 1,
  "bomId": 1,
  "routingId": 1,
  "assignedId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mrpeasy/latest/actions/create-manufacturing-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "articleId": 1,
    "quantity": 1,
    "bomId": 1,
    "routingId": 1,
    "assignedId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `articleId` | number | yes | MRPeasy article ID to manufacture. |
| `quantity` | number | yes | Manufacturing quantity. |
| `bomId` | number | yes | MRPeasy BOM ID. |
| `routingId` | number | yes | MRPeasy routing ID. |
| `assignedId` | number | yes | MRPeasy assigned user ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native MRPeasy API returns.

## Native endpoint

Through the native MRPeasy API, this operation is `POST /manufacturing-orders` (base URL `https://api.mrpeasy.com/rest/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-manufacturing-order.md) for the provider-specific parameters and requirements.

