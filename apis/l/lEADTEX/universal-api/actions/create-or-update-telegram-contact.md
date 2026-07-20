# LEADTEX: Create Or Update Telegram Contact

Creates or updates a Telegram contact in LEADTEX.

```
PUT https://connect.mindcloud.co/v1/universal/lEADTEX/latest/actions/create-or-update-telegram-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LEADTEX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/lEADTEX/latest/actions/create-or-update-telegram-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "bot_id": 1,
  "messenger": "telegram",
  "name": "Ava Chen",
  "telegram_id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lEADTEX/latest/actions/create-or-update-telegram-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "bot_id": 1,
    "messenger": "telegram",
    "name": "Ava Chen",
    "telegram_id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `bot_id` | number | yes | ID of the bot to create or update the contact in. |
| `messenger` | string | yes | Use telegram for this action. Default: `telegram`. |
| `name` | string | yes | Contact name. |
| `telegram_id` | number | yes | Telegram user ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "bot_id": 1,
        "created_at": "2026-05-07T12:00:00.000Z",
        "id": 1,
        "messenger": "string",
        "name": "Ava Chen",
        "telegram_id": 1,
        "telegram_username": "Ava Chen"
      },
      "errors": {},
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `data.bot_id` | number |  |
| `data.created_at` | date |  |
| `data.id` | number |  |
| `data.messenger` | string |  |
| `data.name` | string |  |
| `data.telegram_id` | number |  |
| `data.telegram_username` | string |  |
| `errors` | object |  |
| `message` | string |  |

## Native endpoint

Through the native LEADTEX API, this operation is `POST /createOrUpdateContact?api_token={{credentials.apiKey}}` (base URL `https://app.leadteh.ru/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-update-telegram-contact.md) for the provider-specific parameters and requirements.

