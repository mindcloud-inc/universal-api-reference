# Watbot: Queue Broadcast Message

Queues a broadcast message in Watbot.

```
POST https://connect.mindcloud.co/v1/universal/watbot/latest/actions/queue-broadcast-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Watbot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/watbot/latest/actions/queue-broadcast-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "messageId": "string",
  "text": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/watbot/latest/actions/queue-broadcast-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "messageId": "string",
    "text": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `messageId` | string | yes | Уникальный ID сообщения. |
| `text` | string | yes | Текст сообщения. |
| `contactId` | number | no | ID контакта Watbot. Нужен, когда bitrix_contact_id и phone не переданы. |
| `phone` | string | no | Номер телефона получателя. Нужен, когда contact_id и bitrix_contact_id не переданы. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `bitrixContactId` | number | no | ID контакта Битрикса. Нужен, когда contact_id и phone не переданы. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Watbot API returns.

## Native endpoint

Through the native Watbot API, this operation is `POST /sendMessageToQueue` (base URL `https://watbot.ru/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/queue-broadcast-message.md) for the provider-specific parameters and requirements.

