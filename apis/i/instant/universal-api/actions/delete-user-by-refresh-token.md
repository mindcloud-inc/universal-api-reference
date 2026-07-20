# Instant: Delete User by Refresh Token

Deletes a user from Instant by refresh token.

```
DELETE https://connect.mindcloud.co/v1/universal/instant/latest/actions/delete-user-by-refresh-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instant `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/instant/latest/actions/delete-user-by-refresh-token?connectionId=$CONNECTION_ID&refreshToken=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "refreshToken": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instant/latest/actions/delete-user-by-refresh-token?${params}`, {
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
| `refreshToken` | string | yes | Refresh token whose user should be deleted. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deleted": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deleted` | object | Deleted Instant user. |

## Native endpoint

Through the native Instant API, this operation is `DELETE /admin/users` (base URL `https://api.instantdb.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-user-by-refresh-token.md) for the provider-specific parameters and requirements.

