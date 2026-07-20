# Handelsregister AI: Create API Token

Creates a new API token in Handelsregister AI.

```
POST https://connect.mindcloud.co/v1/universal/handelsregisterAI/latest/actions/create-api-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Handelsregister AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/handelsregisterAI/latest/actions/create-api-token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tokenName": "codex-temp-token"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/handelsregisterAI/latest/actions/create-api-token', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tokenName": "codex-temp-token"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tokenName` | string | yes | Name for the API token to create. Example: `codex-temp-token`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `expiresAt` | string | no | Optional token expiration timestamp. Example: `2026-12-31 23:59:59`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "abilities": [
        "string"
      ],
      "created_at": "string",
      "expires_at": "string",
      "meta": {},
      "name": "Ava Chen",
      "token": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `abilities` | array<string> | Token abilities granted by the provider. |
| `created_at` | string | Token creation timestamp. |
| `expires_at` | string | Optional token expiration timestamp. |
| `meta` | object | Provider metadata for the creation request. |
| `name` | string | Created token name. |
| `token` | string | Created API token string. |

## Native endpoint

Through the native Handelsregister AI API, this operation is `POST /auth/tokens/create` (base URL `https://handelsregister.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-api-token.md) for the provider-specific parameters and requirements.

