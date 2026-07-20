# Meetstream AI: Get Bot Status

Retrieves a bot status from Meetstream AI.

```
GET https://connect.mindcloud.co/v1/universal/meetstreamAI/latest/actions/get-bot-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Meetstream AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/meetstreamAI/latest/actions/get-bot-status?connectionId=$CONNECTION_ID&botId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "botId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/meetstreamAI/latest/actions/get-bot-status?${params}`, {
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
| `botId` | string | yes | The bot identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "botId": "string",
      "customAttributes": {},
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `botId` | string | Bot identifier. |
| `customAttributes` | object | Custom attributes attached to the bot. |
| `status` | string | Current bot status. |

## Native endpoint

Through the native Meetstream AI API, this operation is `GET /bots/:bot_id/status` (base URL `https://api.meetstream.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-bot-status.md) for the provider-specific parameters and requirements.

