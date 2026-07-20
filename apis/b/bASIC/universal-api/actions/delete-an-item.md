# BASIC: Delete an item

Deletes an existing item from a BASIC table.

```
DELETE https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/delete-an-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BASIC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/delete-an-item?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/delete-an-item?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native BASIC API returns.

## Native endpoint

Through the native BASIC API, this operation is `DELETE /project/{id}/user/{user_id}/db/{table_id}/{item_id}` (base URL `https://api.basic.tech`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-an-item.md) for the provider-specific parameters and requirements.

