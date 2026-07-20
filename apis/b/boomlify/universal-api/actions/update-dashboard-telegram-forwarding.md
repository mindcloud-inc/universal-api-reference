# Boomlify: Update Dashboard Telegram Forwarding

Updates Telegram forwarding for an owned mailbox in Boomlify.

```
PUT https://connect.mindcloud.co/v1/universal/boomlify/latest/actions/update-dashboard-telegram-forwarding
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Boomlify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/boomlify/latest/actions/update-dashboard-telegram-forwarding" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "isEnabled": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/boomlify/latest/actions/update-dashboard-telegram-forwarding', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "isEnabled": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Boomlify dashboard email UUID. |
| `isEnabled` | boolean | yes | Whether Telegram forwarding should be enabled. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "emailId": "ava@example.com",
      "id": "string",
      "isEnabled": true,
      "status": "string",
      "telegramChatId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `emailId` | string | Dashboard email identifier. |
| `id` | string | Telegram forwarding configuration identifier. |
| `isEnabled` | boolean | Whether Telegram forwarding is enabled. |
| `status` | string | Update operation status. |
| `telegramChatId` | string | Telegram chat identifier when available. |

## Native endpoint

Through the native Boomlify API, this operation is `POST /api/v1/emails/{id}/telegram-forwarding` (base URL `https://v1.boomlify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-dashboard-telegram-forwarding.md) for the provider-specific parameters and requirements.

