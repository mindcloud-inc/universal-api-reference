# Product Fruits: Delete User



```
DELETE https://connect.mindcloud.co/v1/universal/productFruits/latest/actions/delete-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Product Fruits `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/productFruits/latest/actions/delete-user?connectionId=$CONNECTION_ID&username=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "username": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/productFruits/latest/actions/delete-user?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `username` | string | yes | Username of the tracked user to delete. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Product Fruits API returns.

## Native endpoint

Through the native Product Fruits API, this operation is `DELETE /v1/users/:username` (base URL `https://api.productfruits.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-user.md) for the provider-specific parameters and requirements.

