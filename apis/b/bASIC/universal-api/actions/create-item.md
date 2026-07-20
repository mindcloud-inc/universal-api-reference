# BASIC: Create item

Creates a new item in a BASIC table.

```
POST https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/create-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BASIC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/create-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/create-item', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native BASIC API returns.

## Native endpoint

Through the native BASIC API, this operation is `POST /project/{id}/user/{user_id}/db/{table_id}` (base URL `https://api.basic.tech`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-item.md) for the provider-specific parameters and requirements.

