# Parsio: Create Webhook



```
POST https://connect.mindcloud.co/v1/universal/parsio/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Parsio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/parsio/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "mailboxId": "string",
  "url": "https://example.com",
  "event": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/parsio/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "mailboxId": "string",
    "url": "https://example.com",
    "event": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `mailboxId` | string | yes | Parsio mailbox ID. |
| `url` | string | yes | Destination webhook URL. |
| `event` | string | yes | Trigger event. |
| `enabled` | boolean | no | Whether the webhook is enabled. |
| `tableId` | string | no | Table ID for table.parsed events. Default: `default`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "enabled": true,
      "event": "string",
      "mailboxId": "string",
      "name": "Ava Chen",
      "ownerId": "string",
      "tableId": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | Webhook creation timestamp. |
| `enabled` | boolean | Whether the webhook is enabled. |
| `event` | string | Webhook event. |
| `mailboxId` | string | Mailbox ID. |
| `name` | string | Webhook name. |
| `ownerId` | string | Webhook owner ID. |
| `tableId` | string | Webhook table ID. |
| `updatedAt` | date | Webhook update timestamp. |
| `url` | string | Webhook destination URL. |

## Native endpoint

Through the native Parsio API, this operation is `POST /webhooks/:mailbox_id` (base URL `https://api.parsio.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

