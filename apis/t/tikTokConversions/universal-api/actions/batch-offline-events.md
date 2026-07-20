# TikTok Conversions: Batch Offline Events

Reports offline events in bulk to TikTok Conversions.

```
POST https://connect.mindcloud.co/v1/universal/tikTokConversions/latest/actions/batch-offline-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TikTok Conversions `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tikTokConversions/latest/actions/batch-offline-events" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "event_set_id": "string",
  "batch[].event": "string",
  "batch[].timestamp": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tikTokConversions/latest/actions/batch-offline-events', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "event_set_id": "string",
    "batch[].event": "string",
    "batch[].timestamp": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `event_set_id` | string | yes |  |
| `batch[].event` | string | yes |  |
| `batch[].event_id` | string | no |  |
| `batch[].timestamp` | number | yes |  |
| `batch[].context.user.emails[]` | array<string> | no |  |
| `batch[].context.user.phone_numbers[]` | array<string> | no |  |
| `batch[].properties.order_id` | string | no |  |
| `batch[].properties.shop_id` | string | no |  |
| `batch[].properties.currency` | string | no |  |
| `batch[].properties.value` | number | no |  |
| `batch[].properties.event_channel` | string | no |  |
| `batch[].properties.contents[].content_id` | string | no |  |
| `batch[].properties.contents[].quantity` | number | no |  |
| `batch[].properties.contents[].price` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "data": {},
      "message": "string",
      "request_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `data` | object |  |
| `message` | string |  |
| `request_id` | string |  |

## Native endpoint

Through the native TikTok Conversions API, this operation is `POST /open_api/v1.3/offline/batch/` (base URL `https://business-api.tiktok.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/batch-offline-events.md) for the provider-specific parameters and requirements.

