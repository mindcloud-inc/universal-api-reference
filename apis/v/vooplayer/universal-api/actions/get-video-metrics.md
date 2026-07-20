# Vooplayer: Get Video Metrics

Retrieves video analytics data from Vooplayer.

```
GET https://connect.mindcloud.co/v1/universal/vooplayer/latest/actions/get-video-metrics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vooplayer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vooplayer/latest/actions/get-video-metrics?connectionId=$CONNECTION_ID&videoId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "videoId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vooplayer/latest/actions/get-video-metrics?${params}`, {
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
| `videoId` | number | yes | Video ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completitionRate": 1,
      "loads": 1,
      "playRate": 1,
      "plays": 1,
      "shares": 1,
      "watched": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completitionRate` | number | Completion rate. |
| `loads` | number | Total video loads. |
| `playRate` | number | Play rate. |
| `plays` | number | Total plays. |
| `shares` | number | Share count. |
| `watched` | number | Watched percentage. |

## Native endpoint

Through the native Vooplayer API, this operation is `GET /api/video/metrics` (base URL `https://api.spotlightr.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-video-metrics.md) for the provider-specific parameters and requirements.

