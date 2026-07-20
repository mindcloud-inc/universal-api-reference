# Smartcar: Remove User

Deletes an existing user from Smartcar.

```
DELETE https://connect.mindcloud.co/v1/universal/smartcar/latest/actions/remove-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smartcar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/smartcar/latest/actions/remove-user?connectionId=$CONNECTION_ID&userId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartcar/latest/actions/remove-user?${params}`, {
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
| `userId` | string | yes | The Smartcar user ID to delete. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Smartcar API returns.

## Native endpoint

Through the native Smartcar API, this operation is `DELETE /users/:userId` (base URL `https://vehicle.api.smartcar.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-user.md) for the provider-specific parameters and requirements.

