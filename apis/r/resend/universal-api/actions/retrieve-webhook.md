# Resend: Retrieve Webhook

Retrieves a webhook from Resend.

```
GET https://connect.mindcloud.co/v1/universal/resend/latest/actions/retrieve-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Resend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/resend/latest/actions/retrieve-webhook?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/resend/latest/actions/retrieve-webhook?${params}`, {
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
| `id` | list<string> | yes | The unique identifier of the webhook to retrieve |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "endpoint": "string",
      "events": [
        "string"
      ],
      "id": "string",
      "object": "string",
      "signingSecret": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | When the webhook was created. |
| `endpoint` | string | Webhook endpoint URL. |
| `events` | array<string> | Subscribed event types. |
| `id` | string | Webhook identifier. |
| `object` | string | Object type identifier. |
| `signingSecret` | string | Webhook signing secret. |
| `status` | string | Webhook status. |

## Native endpoint

Through the native Resend API, this operation is `GET /webhooks/:id` (base URL `https://api.resend.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-webhook.md) for the provider-specific parameters and requirements.

