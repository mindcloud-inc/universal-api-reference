# Instant: Create Refresh Token by Email With Extra Fields

Creates a refresh token in Instant by email, setting extra fields on user creation.

```
POST https://connect.mindcloud.co/v1/universal/instant/latest/actions/create-refresh-token-by-email-with-extra-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instant `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/instant/latest/actions/create-refresh-token-by-email-with-extra-fields" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/instant/latest/actions/create-refresh-token-by-email-with-extra-fields', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | User email address to issue a refresh token for. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `extraFields` | object | no | Optional custom $users fields to set when creating the user. |

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

Through the native Instant API, this operation is `POST /admin/refresh_tokens` (base URL `https://api.instantdb.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-refresh-token-by-email-with-extra-fields.md) for the provider-specific parameters and requirements.

