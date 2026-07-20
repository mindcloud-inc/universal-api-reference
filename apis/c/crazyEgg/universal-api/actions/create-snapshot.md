# Crazy Egg: Create Snapshot



```
POST https://connect.mindcloud.co/v1/universal/crazyEgg/latest/actions/create-snapshot
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crazy Egg `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/crazyEgg/latest/actions/create-snapshot" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "snapshot.sourceUrl": "https://example.com",
  "snapshot.name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/crazyEgg/latest/actions/create-snapshot', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "snapshot.sourceUrl": "https://example.com",
    "snapshot.name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `snapshot.sourceUrl` | string | yes |  |
| `snapshot.name` | string | yes |  |
| `snapshot.maxVisits` | number | no |  |
| `snapshot.expiresAt` | number | no |  |
| `snapshot.startsAt` | number | no |  |
| `snapshot.description` | string | no |  |
| `snapshot.urlMatchingRules` | string | no |  |
| `snapshot.samplingRatio` | number | no |  |
| `snapshot.device` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "device": "string",
      "expires_at": "string",
      "heatmap_generation_status": "string",
      "heatmap_url": "https://example.com",
      "id": "string",
      "max_visits": 1,
      "name": "Ava Chen",
      "processing_status": "string",
      "sampling_ratio": 1,
      "screenshot_url": "https://example.com",
      "source_url": "https://example.com",
      "starts_at": "string",
      "status": "string",
      "thumbnail_url": "https://example.com",
      "url_matching_rules": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `device` | string |  |
| `expires_at` | string |  |
| `heatmap_generation_status` | string |  |
| `heatmap_url` | string |  |
| `id` | string |  |
| `max_visits` | number |  |
| `name` | string |  |
| `processing_status` | string |  |
| `sampling_ratio` | number |  |
| `screenshot_url` | string |  |
| `source_url` | string |  |
| `starts_at` | string |  |
| `status` | string |  |
| `thumbnail_url` | string |  |
| `url_matching_rules` | string |  |

## Native endpoint

Through the native Crazy Egg API, this operation is `POST /snapshots.json` (base URL `https://app.crazyegg.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-snapshot.md) for the provider-specific parameters and requirements.

