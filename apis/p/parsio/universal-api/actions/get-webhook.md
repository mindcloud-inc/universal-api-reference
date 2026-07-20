# Parsio: Get Webhook



```
GET https://connect.mindcloud.co/v1/universal/parsio/latest/actions/get-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Parsio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/parsio/latest/actions/get-webhook?connectionId=$CONNECTION_ID&webhookId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "webhookId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/parsio/latest/actions/get-webhook?${params}`, {
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
| `webhookId` | string | yes | Parsio webhook ID. |

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
| `event` | string | Trigger event. |
| `mailboxId` | string | Mailbox ID. |
| `name` | string | Webhook name. |
| `ownerId` | string | Webhook owner ID. |
| `tableId` | string | Webhook table ID. |
| `updatedAt` | date | Webhook update timestamp. |
| `url` | string | Destination webhook URL. |

## Native endpoint

Through the native Parsio API, this operation is `GET /webhooks/:webhook_id` (base URL `https://api.parsio.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-webhook.md) for the provider-specific parameters and requirements.

