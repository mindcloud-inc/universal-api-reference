# Cloud BOT: List Bot Subscriptions

Retrieves bot subscriptions from Cloud BOT.

```
GET https://connect.mindcloud.co/v1/universal/cloudBOT/latest/actions/list-bot-subscriptions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloud BOT `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudBOT/latest/actions/list-bot-subscriptions?connectionId=$CONNECTION_ID&publicId=string&botId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "publicId": "string",
  "botId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudBOT/latest/actions/list-bot-subscriptions?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "callbackEmails": {},
      "callbackEndpoint": "string",
      "callbackType": "string",
      "code": 1,
      "disabled": true,
      "event": "string",
      "language": "string",
      "subscribeId": 1,
      "unsubscribeEndpoint": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `callbackEmails` | object | Callback email settings for mailhook subscriptions |
| `callbackEndpoint` | string | Callback endpoint URL |
| `callbackType` | string | Callback type |
| `code` | number | Response status code |
| `disabled` | boolean | Whether the subscription is disabled |
| `event` | string | Subscription event |
| `language` | string | Subscription language |
| `subscribeId` | number | Subscription ID |
| `unsubscribeEndpoint` | string | Endpoint used to unsubscribe |

## Native endpoint

Through the native Cloud BOT API, this operation is `GET /:public_id/bots/:bot_id/subscriptions` (base URL `https://api.c-bot.pro`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-bot-subscriptions.md) for the provider-specific parameters and requirements.

