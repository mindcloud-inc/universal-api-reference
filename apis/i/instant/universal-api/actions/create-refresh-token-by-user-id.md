# Instant: Create Refresh Token by User ID

Creates a refresh token in Instant by user ID.

```
POST https://connect.mindcloud.co/v1/universal/instant/latest/actions/create-refresh-token-by-user-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instant `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/instant/latest/actions/create-refresh-token-by-user-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/instant/latest/actions/create-refresh-token-by-user-id', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Instant user ID to issue a refresh token for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": true,
      "user": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | boolean | Whether a new user was created. |
| `user` | object | Instant user with the issued refresh token. |

## Native endpoint

Through the native Instant API, this operation is `POST /admin/refresh_tokens` (base URL `https://api.instantdb.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-refresh-token-by-user-id.md) for the provider-specific parameters and requirements.

