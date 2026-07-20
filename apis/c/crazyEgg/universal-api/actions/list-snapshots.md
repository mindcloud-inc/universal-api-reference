# Crazy Egg: List Snapshots



```
GET https://connect.mindcloud.co/v1/universal/crazyEgg/latest/actions/list-snapshots
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crazy Egg `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crazyEgg/latest/actions/list-snapshots?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crazyEgg/latest/actions/list-snapshots?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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

Through the native Crazy Egg API, this operation is `GET /snapshots.json` (base URL `https://app.crazyegg.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-snapshots.md) for the provider-specific parameters and requirements.

