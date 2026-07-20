# folk: Get Webhook

Retrieves a specific webhook from folk.

```
GET https://connect.mindcloud.co/v1/universal/folk/latest/actions/get-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a folk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/folk/latest/actions/get-webhook?connectionId=$CONNECTION_ID&webhookId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "webhookId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/folk/latest/actions/get-webhook?${params}`, {
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
| `webhookId` | string | yes | The ID of the webhook to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "redactedSigningSecret": "string",
      "status": "string",
      "subscribedEvents": [
        {}
      ],
      "targetUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `id` | string |  |
| `name` | string |  |
| `redactedSigningSecret` | string |  |
| `status` | string |  |
| `subscribedEvents` | array<object> |  |
| `targetUrl` | string |  |

## Native endpoint

Through the native folk API, this operation is `GET /v1/webhooks/:webhookId` (base URL `https://api.folk.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-webhook.md) for the provider-specific parameters and requirements.

