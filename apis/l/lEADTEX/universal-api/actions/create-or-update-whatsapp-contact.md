# LEADTEX: Create Or Update WhatsApp Contact

Creates or updates a WhatsApp contact in LEADTEX.

```
PUT https://connect.mindcloud.co/v1/universal/lEADTEX/latest/actions/create-or-update-whatsapp-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LEADTEX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/lEADTEX/latest/actions/create-or-update-whatsapp-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "bot_id": 1,
  "messenger": "whatsapp",
  "name": "Ava Chen",
  "phone": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lEADTEX/latest/actions/create-or-update-whatsapp-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "bot_id": 1,
    "messenger": "whatsapp",
    "name": "Ava Chen",
    "phone": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `bot_id` | number | yes | ID of the bot to create or update the contact in. |
| `messenger` | string | yes | Use whatsapp for this action. Default: `whatsapp`. |
| `name` | string | yes | Contact name. |
| `phone` | string | yes | WhatsApp phone number in international format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "bot_id": 1,
        "created_at": "2026-05-07T12:00:00.000Z",
        "email": "ava@example.com",
        "id": 1,
        "messenger": "string",
        "name": "Ava Chen",
        "phone": "string"
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
| `data.email` | string |  |
| `data.id` | number |  |
| `data.messenger` | string |  |
| `data.name` | string |  |
| `data.phone` | string |  |
| `errors` | object |  |
| `message` | string |  |

## Native endpoint

Through the native LEADTEX API, this operation is `POST /createOrUpdateContact?api_token={{credentials.apiKey}}` (base URL `https://app.leadteh.ru/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-update-whatsapp-contact.md) for the provider-specific parameters and requirements.

