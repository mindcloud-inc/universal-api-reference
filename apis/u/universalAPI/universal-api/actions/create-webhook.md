# Universal API: Create Webhook

Creates a new webhook in Universal API.

```
POST https://connect.mindcloud.co/v1/universal/universalAPI/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Universal API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/universalAPI/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "unifiedApi": "ATS",
  "deliveryUrl": "https://example.com",
  "status": "Disabled",
  "events[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/universalAPI/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "unifiedApi": "ATS",
    "deliveryUrl": "https://example.com",
    "status": "Disabled",
    "events[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `unifiedApi` | list<string> | yes | Unified API category for the webhook. One of: `ATS`, `HRIS`. |
| `deliveryUrl` | string | yes | Webhook delivery URL. |
| `status` | list<string> | yes | Webhook status. One of: `Disabled`, `Enabled`. |
| `events[]` | array<string> | yes | Webhook event names. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "event": "string",
      "id": "string",
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
| `event` | string |  |
| `id` | string |  |
| `status` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Universal API API, this operation is `POST /api/webhooks` (base URL `https://api.prod.universalapi.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

