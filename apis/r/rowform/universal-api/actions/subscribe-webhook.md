# Rowform: Subscribe Webhook

Creates a webhook subscription in Rowform.

```
POST https://connect.mindcloud.co/v1/universal/rowform/latest/actions/subscribe-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rowform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rowform/latest/actions/subscribe-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "hookUrl": "https://example.com",
  "event": "form.response.created",
  "formId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rowform/latest/actions/subscribe-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "hookUrl": "https://example.com",
    "event": "form.response.created",
    "formId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `hookUrl` | string | yes | The HTTPS URL that Rowform should POST webhook deliveries to. |
| `event` | string | yes | The Rowform event type to subscribe to. The current public docs show form.response.created. Default: `form.response.created`. |
| `formId` | string | yes | The Rowform form id that should emit webhook events. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `message` | string |  |

## Native endpoint

Through the native Rowform API, this operation is `POST /api/zapier/hooks` (base URL `https://app.rowform.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/subscribe-webhook.md) for the provider-specific parameters and requirements.

