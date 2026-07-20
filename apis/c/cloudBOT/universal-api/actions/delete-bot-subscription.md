# Cloud BOT: Delete Bot Subscription

Deletes a bot subscription from Cloud BOT.

```
DELETE https://connect.mindcloud.co/v1/universal/cloudBOT/latest/actions/delete-bot-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloud BOT `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/cloudBOT/latest/actions/delete-bot-subscription?connectionId=$CONNECTION_ID&publicId=string&botId=string&subscribeId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "publicId": "string",
  "botId": "string",
  "subscribeId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudBOT/latest/actions/delete-bot-subscription?${params}`, {
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
| `publicId` | string | yes |  |
| `botId` | string | yes |  |
| `subscribeId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number | Response status code |

## Native endpoint

Through the native Cloud BOT API, this operation is `DELETE /:public_id/bots/:bot_id/subscriptions/:subscribe_id` (base URL `https://api.c-bot.pro`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-bot-subscription.md) for the provider-specific parameters and requirements.

