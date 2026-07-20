# Watbot: Send Message By External ID

Creates a new message in Watbot by external contact ID.

```
POST https://connect.mindcloud.co/v1/universal/watbot/latest/actions/send-message-by-external-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Watbot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/watbot/latest/actions/send-message-by-external-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "botId": 1,
  "contactExternalId": "string",
  "messenger": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/watbot/latest/actions/send-message-by-external-id', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "botId": 1,
    "contactExternalId": "string",
    "messenger": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `botId` | number | yes | ID бота контакта. |
| `contactExternalId` | string | yes | Номер телефона или внешний ID контакта в мессенджере. |
| `messenger` | string | yes | whatsapp, telegram, viber, vk или max. |
| `text` | string | no | Сообщение. Передайте text, image или file. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `image` | string | no | URL на картинку. |
| `file` | string | no | URL на файл. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | True when the message is accepted by Watbot. |

## Native endpoint

Through the native Watbot API, this operation is `POST /sendMessage` (base URL `https://watbot.ru/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-message-by-external-id.md) for the provider-specific parameters and requirements.

