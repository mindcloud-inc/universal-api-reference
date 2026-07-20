# Watbot: List Contacts

Retrieves contacts from Watbot.

```
GET https://connect.mindcloud.co/v1/universal/watbot/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Watbot `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/watbot/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/watbot/latest/actions/list-contacts?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dateFrom` | number | no | Фильтр по дате создания контакта в формате Unix Time. |
| `dateTo` | number | no | Фильтр по дате создания контакта в формате Unix Time. |
| `botId` | number | no | ID бота. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "bot_id": 1,
      "created_at": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "id": 1,
      "messenger": "string",
      "name": "Ava Chen",
      "phone": "string",
      "telegram_id": "string",
      "telegram_username": "Ava Chen",
      "utm": {},
      "viber_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string | Адрес контакта. |
| `bot_id` | number | ID бота контакта. |
| `created_at` | date | Дата создания контакта. |
| `email` | string | Email контакта. |
| `id` | number | ID контакта. |
| `messenger` | string | Мессенджер контакта. |
| `name` | string | Имя контакта. |
| `phone` | string | Телефон контакта. |
| `telegram_id` | string | ID пользователя в Telegram. |
| `telegram_username` | string | Username пользователя в Telegram. |
| `utm` | object | UTM-метки контакта. |
| `viber_id` | string | ID пользователя в Viber. |

## Native endpoint

Through the native Watbot API, this operation is `GET /getContacts` (base URL `https://watbot.ru/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

