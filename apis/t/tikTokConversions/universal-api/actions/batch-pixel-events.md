# TikTok Conversions: Batch Pixel Events

Tracks Pixel events in bulk in TikTok Conversions.

```
POST https://connect.mindcloud.co/v1/universal/tikTokConversions/latest/actions/batch-pixel-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TikTok Conversions `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tikTokConversions/latest/actions/batch-pixel-events" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "batch[].event": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tikTokConversions/latest/actions/batch-pixel-events', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "batch[].event": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `batch[].event` | string | yes |  |
| `batch[].event_id` | string | no |  |
| `batch[].timestamp` | number | no |  |
| `batch[].context.ad.callback` | string | no |  |
| `batch[].context.page.url` | string | no |  |
| `batch[].context.page.referrer` | string | no |  |
| `batch[].context.user.external_id` | string | no |  |
| `batch[].context.user.email` | string | no |  |
| `batch[].context.user.phone_number` | string | no |  |
| `batch[].context.user.ttp` | string | no |  |
| `batch[].context.ip` | string | no |  |
| `batch[].context.user_agent` | string | no |  |
| `batch[].properties.content_type` | string | no |  |
| `batch[].properties.currency` | string | no |  |
| `batch[].properties.value` | number | no |  |
| `batch[].properties.query` | string | no |  |
| `batch[].properties.description` | string | no |  |
| `batch[].properties.status` | string | no |  |
| `batch[].properties.contents[].price` | number | no |  |
| `batch[].properties.contents[].quantity` | number | no |  |
| `batch[].properties.contents[].content_id` | string | no |  |
| `batch[].properties.contents[].content_category` | string | no |  |
| `batch[].properties.contents[].content_name` | string | no |  |
| `batch[].properties.contents[].brand` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "data": {
        "failed_events": [
          [
            {}
          ]
        ],
        "partial_failure": true
      },
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
| `data.failed_events[]` | array<object> |  |
| `data.failed_events[].error` | string |  |
| `data.failed_events[].order_in_batch` | number |  |
| `data.partial_failure` | boolean |  |
| `message` | string |  |
| `request_id` | string |  |

## Native endpoint

Through the native TikTok Conversions API, this operation is `POST /open_api/v1.3/pixel/batch/` (base URL `https://business-api.tiktok.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/batch-pixel-events.md) for the provider-specific parameters and requirements.

