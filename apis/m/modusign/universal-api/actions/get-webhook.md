# Modusign: Get Webhook

Retrieves a webhook from Modusign.

```
GET https://connect.mindcloud.co/v1/universal/modusign/latest/actions/get-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Modusign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/modusign/latest/actions/get-webhook?connectionId=$CONNECTION_ID&webhookId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "webhookId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/modusign/latest/actions/get-webhook?${params}`, {
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
| `webhookId` | string | yes | The Modusign webhook ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "events": [
        "string"
      ],
      "headers": [
        {}
      ],
      "id": "string",
      "name": "Ava Chen",
      "updatedAt": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string | The creation timestamp. |
| `events` | array<string> | Subscribed webhook events. |
| `headers` | array<object> | Additional webhook headers. |
| `id` | string | The webhook ID. |
| `name` | string | The webhook name. |
| `updatedAt` | string | The update timestamp. |
| `url` | string | The webhook callback URL. |

## Native endpoint

Through the native Modusign API, this operation is `GET /webhooks/:webhookId` (base URL `https://api.modusign.co.kr`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-webhook.md) for the provider-specific parameters and requirements.

