# NetExplorer: Delete User Picture



```
DELETE https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/delete-user-by-user-id-picture
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetExplorer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/delete-user-by-user-id-picture?connectionId=$CONNECTION_ID&userId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/delete-user-by-user-id-picture?${params}`, {
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
| `userId` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native NetExplorer API returns.

## Native endpoint

Through the native NetExplorer API, this operation is `DELETE /user/:userId/picture` (base URL `{{credentials.platformBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-user-by-user-id-picture.md) for the provider-specific parameters and requirements.

