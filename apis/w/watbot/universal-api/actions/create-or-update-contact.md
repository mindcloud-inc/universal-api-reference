# Watbot: Create Or Update Contact

Finds a contact in Watbot, or creates one if no match is found.

```
POST https://connect.mindcloud.co/v1/universal/watbot/latest/actions/create-or-update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Watbot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/watbot/latest/actions/create-or-update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "botId": 1,
  "messenger": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/watbot/latest/actions/create-or-update-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "botId": 1,
    "messenger": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `botId` | number | yes | ID бота. |
| `messenger` | string | yes | Тип мессенджера. Поддерживаются whatsapp, telegram, viber и vk. |
| `name` | string | yes | Имя контакта. |
| `phone` | string | no | Номер телефона в международном формате. Обязателен для messenger=whatsapp. |
| `telegramId` | number | no | ID пользователя в Telegram. Обязателен для Telegram. |
| `telegramUsername` | string | no | Username пользователя Telegram. |
| `viberId` | string | no | ID пользователя в Viber. Обязателен для Viber. |
| `vkId` | number | no | ID пользователя во ВКонтакте. Обязателен для VK. |
| `email` | string | no | Email контакта. |
| `address` | string | no | Адрес контакта. |
| `tags[]` | array<string> | no | Массив тегов контакта. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Watbot API returns.

## Native endpoint

Through the native Watbot API, this operation is `POST /createOrUpdateContact` (base URL `https://watbot.ru/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-update-contact.md) for the provider-specific parameters and requirements.

