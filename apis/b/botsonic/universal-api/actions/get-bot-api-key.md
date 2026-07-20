# Botsonic: Get Bot API Key

Retrieves a bot API key from Botsonic.

```
GET https://connect.mindcloud.co/v1/universal/botsonic/latest/actions/get-bot-api-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Botsonic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/botsonic/latest/actions/get-bot-api-key?connectionId=$CONNECTION_ID&botId=bot_123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "botId": "bot_123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/botsonic/latest/actions/get-bot-api-key?${params}`, {
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
| `botId` | string | yes | bot_id of the bot. Example: `bot_123`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceId` | string | no | Optional workspace identifier. Example: `workspace_123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bot_api_type": "string",
      "bot_id": "string",
      "created_at": "string",
      "end_user_rate_limit": 1,
      "id": "string",
      "token": "string",
      "updated_at": "string",
      "whitelisted_hosts": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bot_api_type` | string | Bot API token type. |
| `bot_id` | string | Bot identifier. |
| `created_at` | string | Creation timestamp. |
| `end_user_rate_limit` | number | End-user rate limit. |
| `id` | string | API key identifier. |
| `token` | string | Bot API token. |
| `updated_at` | string | Last update timestamp. |
| `whitelisted_hosts` | array<string> | Whitelisted hosts. |

## Native endpoint

Through the native Botsonic API, this operation is `GET /v1/business/bot/:botId/bot-api-key` (base URL `https://api.botsonic.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-bot-api-key.md) for the provider-specific parameters and requirements.

