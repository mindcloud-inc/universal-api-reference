# Reddit Lead Ads: Post Conversion Events

Creates conversion events for a Reddit pixel.

```
POST https://connect.mindcloud.co/v1/universal/redditAds/latest/actions/post-conversion-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reddit Lead Ads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/redditAds/latest/actions/post-conversion-events" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "pixelId": "string",
  "data": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/redditAds/latest/actions/post-conversion-events', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "pixelId": "string",
    "data": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `pixelId` | string | yes | Reddit Ads pixel identifier. |
| `data` | object | yes | JSON request body from the Reddit Ads API spec. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Conversion event identifier. |
| `status` | string | Conversion event status. |

## Native endpoint

Through the native Reddit Lead Ads API, this operation is `POST /pixels/{pixel_id}/conversion_events` (base URL `https://ads-api.reddit.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/post-conversion-events.md) for the provider-specific parameters and requirements.

