# Watbot: Send Message To WhatsApp

Creates a new WhatsApp message in Watbot.

```
POST https://connect.mindcloud.co/v1/universal/watbot/latest/actions/send-message-to-whats-app
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Watbot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/watbot/latest/actions/send-message-to-whats-app" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "botId": 1,
  "phone": "string",
  "text": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/watbot/latest/actions/send-message-to-whats-app', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "botId": 1,
    "phone": "string",
    "text": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `botId` | number | yes | ID бота контакта. |
| `phone` | string | yes | Номер телефона. |
| `text` | string | yes | Сообщение. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | no | Имя контакта. Передавайте при первом сообщении на этот номер. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Watbot API returns.

## Native endpoint

Through the native Watbot API, this operation is `POST /sendMessageToWhatsApp` (base URL `https://watbot.ru/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-message-to-whats-app.md) for the provider-specific parameters and requirements.

