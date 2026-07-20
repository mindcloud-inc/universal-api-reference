# Wistia: Get Media Aggregated Stats

Retrieves aggregated stats for a Wistia media item.

```
GET https://connect.mindcloud.co/v1/universal/wistia/latest/actions/get-media-aggregated-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wistia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wistia/latest/actions/get-media-aggregated-stats?connectionId=$CONNECTION_ID&mediaHashedId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "mediaHashedId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wistia/latest/actions/get-media-aggregated-stats?${params}`, {
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
| `mediaHashedId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actions": [
        {
          "actionCount": 1,
          "impressionCount": 1,
          "rate": 1,
          "type": "string"
        }
      ],
      "engagement": 1,
      "hoursWatched": 1,
      "loadCount": 1,
      "playCount": 1,
      "playRate": 1,
      "visitors": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actions` | array<object> |  |
| `actions[].actionCount` | number | Number of actions performed. |
| `actions[].impressionCount` | number | Number of times the action was shown. |
| `actions[].rate` | number | The rate of actions performed over impressions. |
| `actions[].type` | string | Type of action (e.g., "Call to Action"). |
| `engagement` | number | The average percentage of the video that gets viewed (between 0 and 1). |
| `hoursWatched` | number | The total time spent watching this video. |
| `loadCount` | number | The total number of times this video has been loaded. |
| `playCount` | number | The total number of times this video has been played. |
| `playRate` | number | The percentage of visitors who clicked play (between 0 and 1). |
| `visitors` | number | The total number of unique people that have loaded this video. |

## Native endpoint

Through the native Wistia API, this operation is `GET /stats/medias/:mediaHashedId.json` (base URL `https://api.wistia.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-media-aggregated-stats.md) for the provider-specific parameters and requirements.

