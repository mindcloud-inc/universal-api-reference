# Airzone Cloud: Create Session Token Pair

Creates a session token pair in Airzone Cloud.

```
POST https://connect.mindcloud.co/v1/universal/airzoneCloud/latest/actions/create-session-token-pair
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Airzone Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/airzoneCloud/latest/actions/create-session-token-pair" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "password": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/airzoneCloud/latest/actions/create-session-token-pair', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "password": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Airzone Cloud account email used to create a session token pair. |
| `password` | string | yes | Airzone Cloud account password used to create a session token pair. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "config": {},
      "confirmation_date": "string",
      "created_at": "string",
      "data": {},
      "email": "ava@example.com",
      "migrated": true,
      "pendingMigration": true,
      "refreshToken": "string",
      "token": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string | User identifier. |
| `config` | object | User configuration. |
| `confirmation_date` | string | Confirmation timestamp. |
| `created_at` | string | Account creation timestamp. |
| `data` | object | User data projection. |
| `email` | string | User email. |
| `migrated` | boolean | Whether the user has just been migrated. |
| `pendingMigration` | boolean | Whether account migration is still in progress. |
| `refreshToken` | string | Refresh token for issuing a new token pair. |
| `token` | string | JWT access token for secured requests. |

## Native endpoint

Through the native Airzone Cloud API, this operation is `POST /auth/login` (base URL `https://m.airzonecloud.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-session-token-pair.md) for the provider-specific parameters and requirements.

