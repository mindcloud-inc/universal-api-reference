# Ablefy: Create Order

Creates a new order in Ablefy.

```
POST https://connect.mindcloud.co/v1/universal/ablefy/latest/actions/create-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ablefy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ablefy/latest/actions/create-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "productId": 1,
  "email": "ava@example.com",
  "firstName": "Ava",
  "lastName": "Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ablefy/latest/actions/create-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "productId": 1,
    "email": "ava@example.com",
    "firstName": "Ava",
    "lastName": "Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `productId` | number | yes |  |
| `email` | string | yes |  |
| `firstName` | string | yes |  |
| `lastName` | string | yes |  |
| `ticketDateId` | number | no |  |
| `pid` | number | no |  |
| `prid` | number | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Ablefy API returns.

## Native endpoint

Through the native Ablefy API, this operation is `POST /api/orders` (base URL `https://api.myablefy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-order.md) for the provider-specific parameters and requirements.

