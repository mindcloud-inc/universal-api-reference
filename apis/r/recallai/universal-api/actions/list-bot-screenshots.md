# Recallai: List Bot Screenshots

Retrieves bot screenshots from Recallai by bot ID.

```
GET https://connect.mindcloud.co/v1/universal/recallai/latest/actions/list-bot-screenshots
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recallai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recallai/latest/actions/list-bot-screenshots?connectionId=$CONNECTION_ID&botId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "botId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/recallai/latest/actions/list-bot-screenshots?${params}`, {
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
| `botId` | string | yes | The ID of the bot for which to retrieve the screenshots |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "recorded_at": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `recorded_at` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Recallai API, this operation is `GET /api/v1/bot/:bot_id/screenshots/` (base URL `https://{{credentials.workspaceRegion}}.recall.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-bot-screenshots.md) for the provider-specific parameters and requirements.

