# Boomlify: Bulk Enable Dashboard Telegram Forwarding

Bulk enables Telegram forwarding for owned mailboxes in Boomlify.

```
PUT https://connect.mindcloud.co/v1/universal/boomlify/latest/actions/bulk-enable-dashboard-telegram-forwarding
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Boomlify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/boomlify/latest/actions/bulk-enable-dashboard-telegram-forwarding" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "emailIds[]": [
    "ava@example.com"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/boomlify/latest/actions/bulk-enable-dashboard-telegram-forwarding', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "emailIds[]": ["ava@example.com"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `emailIds[]` | array<string> | yes | Dashboard email UUIDs to enable Telegram forwarding for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "emailId": "ava@example.com",
      "id": "string",
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `emailId` | string | Dashboard email identifier. |
| `id` | string | Bulk operation row identifier. |
| `message` | string | Operation detail message. |
| `status` | string | Forwarding enablement result status. |

## Native endpoint

Through the native Boomlify API, this operation is `POST /api/v1/emails/telegram-forwarding/bulk-enable` (base URL `https://v1.boomlify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-enable-dashboard-telegram-forwarding.md) for the provider-specific parameters and requirements.

