# FillFaster: Subscribe Webhook

Subscribes a webhook URL to a FillFaster form.

```
POST https://connect.mindcloud.co/v1/universal/fillFaster/latest/actions/subscribe-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FillFaster `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fillFaster/latest/actions/subscribe-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "formId": "string",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fillFaster/latest/actions/subscribe-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "formId": "string",
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `events[]` | array<string> | no | Webhook event names to subscribe. |
| `formId` | string | yes | FillFaster form identifier. |
| `url` | string | yes | Webhook destination URL. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": "string",
      "formId": "string",
      "message": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error` | string | Error message when the request fails. |
| `formId` | string | FillFaster form identifier. |
| `message` | string | Success message from FillFaster. |
| `url` | string | Subscribed webhook URL. |

## Native endpoint

Through the native FillFaster API, this operation is `POST /v1/form/:formId/webhook/subscribe` (base URL `https://api.fillfaster.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/subscribe-webhook.md) for the provider-specific parameters and requirements.

