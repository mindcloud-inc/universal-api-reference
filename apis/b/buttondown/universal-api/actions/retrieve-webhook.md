# Buttondown: Retrieve Webhook

Retrieves a webhook from Buttondown.

```
GET https://connect.mindcloud.co/v1/universal/buttondown/latest/actions/retrieve-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Buttondown `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/buttondown/latest/actions/retrieve-webhook?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/buttondown/latest/actions/retrieve-webhook?${params}`, {
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
| `id` | string | yes | Webhook ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creationDate": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "eventTypes": [
        "string"
      ],
      "id": "string",
      "signingKey": "string",
      "status": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creationDate` | date | When the webhook was created in Buttondown. |
| `description` | string | Optional descriptive label stored on the webhook. |
| `eventTypes` | array<string> | Exact Buttondown event types configured for this webhook. |
| `id` | string | Buttondown webhook ID. |
| `signingKey` | string | Webhook signing key when Buttondown returns it. |
| `status` | string | Current webhook status. |
| `url` | string | Destination URL for webhook deliveries. |

## Native endpoint

Through the native Buttondown API, this operation is `GET /webhooks/:id` (base URL `https://api.buttondown.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-webhook.md) for the provider-specific parameters and requirements.

