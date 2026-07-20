# Flexmail: Get Webhook

Retrieves a webhook endpoint from Flexmail.

```
GET https://connect.mindcloud.co/v1/universal/flexmail/latest/actions/get-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flexmail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flexmail/latest/actions/get-webhook?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flexmail/latest/actions/get-webhook?${params}`, {
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
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "enabled": true,
      "event_name": "Ava Chen",
      "id": "string",
      "target_url": "https://example.com",
      "verification_token": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `enabled` | boolean | Whether the webhook is enabled. |
| `event_name` | string | The event name that triggers the webhook. |
| `id` | string | The identifier of the webhook. |
| `target_url` | string | The HTTPS target URL that receives the webhook. |
| `verification_token` | string | The verification token used by the webhook. |

## Native endpoint

Through the native Flexmail API, this operation is `GET /webhooks/{id}` (base URL `https://api.flexmail.eu`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-webhook.md) for the provider-specific parameters and requirements.

