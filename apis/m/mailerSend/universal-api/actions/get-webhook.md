# MailerSend: Get Webhook



```
GET https://connect.mindcloud.co/v1/universal/mailerSend/latest/actions/get-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailerSend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailerSend/latest/actions/get-webhook?connectionId=$CONNECTION_ID&webhookId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "webhookId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailerSend/latest/actions/get-webhook?${params}`, {
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
| `webhookId` | string | yes | ID of the MailerSend webhook. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "domain": {},
      "editable": true,
      "enabled": true,
      "events": [
        "string"
      ],
      "id": "string",
      "name": "Ava Chen",
      "secret": "string",
      "updatedAt": "string",
      "url": "https://example.com",
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string | Webhook creation timestamp. |
| `domain` | object | Domain metadata linked to the webhook. |
| `editable` | boolean | Whether the webhook can be edited. |
| `enabled` | boolean | Whether the webhook is active. |
| `events` | array<string> | MailerSend event types that trigger the webhook. |
| `id` | string | MailerSend webhook ID. |
| `name` | string | Webhook display name. |
| `secret` | string | Webhook signing secret. |
| `updatedAt` | string | Webhook update timestamp. |
| `url` | string | Destination URL for the webhook. |
| `version` | number | Webhook API version. |

## Native endpoint

Through the native MailerSend API, this operation is `GET /webhooks/:webhook_id` (base URL `https://api.mailersend.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-webhook.md) for the provider-specific parameters and requirements.

