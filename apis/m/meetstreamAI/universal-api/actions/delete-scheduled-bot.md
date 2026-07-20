# Meetstream AI: Delete Scheduled Bot

Deletes a scheduled bot from Meetstream AI.

```
DELETE https://connect.mindcloud.co/v1/universal/meetstreamAI/latest/actions/delete-scheduled-bot
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Meetstream AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/meetstreamAI/latest/actions/delete-scheduled-bot?connectionId=$CONNECTION_ID&botId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "botId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/meetstreamAI/latest/actions/delete-scheduled-bot?${params}`, {
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
| `botId` | string | yes | The scheduled bot identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "botId": "string",
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `botId` | string | Scheduled bot identifier. |
| `message` | string | Deletion result message. |

## Native endpoint

Through the native Meetstream AI API, this operation is `DELETE /calendar/scheduled_bots/:bot_id` (base URL `https://api.meetstream.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-scheduled-bot.md) for the provider-specific parameters and requirements.

