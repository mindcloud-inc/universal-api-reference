# Mifiel: Create Webhook

Creates a new webhook endpoint in Mifiel.

```
POST https://connect.mindcloud.co/v1/universal/mifiel/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mifiel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mifiel/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com",
  "callbackType": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mifiel/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com",
    "callbackType": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | Webhook URL endpoint. |
| `callbackType` | string | yes | Type of event that triggers this webhook: document_closed, signer_completed, signer_rejected, or document_deleted. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "callback_type": "string",
      "created_at": "string",
      "id": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `callback_type` | string | Type of events that trigger this webhook |
| `created_at` | string | When webhook was created |
| `id` | string | Unique identifier |
| `url` | string | Webhook URL endpoint |

## Native endpoint

Through the native Mifiel API, this operation is `POST /api/v1/webhooks` (base URL `https://app.mifiel.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

