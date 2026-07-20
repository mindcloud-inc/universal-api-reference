# Hippo Video: Get Video Reports

Retrieves reports for a Hippo Video video.

```
GET https://connect.mindcloud.co/v1/universal/hippoVideo/latest/actions/get-video-reports
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hippo Video `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hippoVideo/latest/actions/get-video-reports?connectionId=$CONNECTION_ID&videoId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "videoId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hippoVideo/latest/actions/get-video-reports?${params}`, {
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
| `videoId` | number | yes | ID of the video |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actions": {
        "annotations": 1,
        "callToActions": 1,
        "comments": 1,
        "endScreens": 1,
        "forms": 1,
        "noOfActions": 1,
        "questions": 1,
        "reactions": 1,
        "replies": 1
      },
      "avgWatchRate": 1,
      "id": 1,
      "playsInPopularRegion": "string",
      "popularRegion": "string",
      "status": 1,
      "totalPageLoads": 1,
      "totalPlays": 1,
      "uniqueUsers": 1,
      "watchRate": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actions` | object |  |
| `actions.annotations` | number |  |
| `actions.callToActions` | number |  |
| `actions.comments` | number |  |
| `actions.endScreens` | number |  |
| `actions.forms` | number |  |
| `actions.noOfActions` | number |  |
| `actions.questions` | number |  |
| `actions.reactions` | number |  |
| `actions.replies` | number |  |
| `avgWatchRate` | number |  |
| `id` | number |  |
| `playsInPopularRegion` | string |  |
| `popularRegion` | string |  |
| `status` | number |  |
| `totalPageLoads` | number |  |
| `totalPlays` | number |  |
| `uniqueUsers` | number |  |
| `watchRate` | object |  |

## Native endpoint

Through the native Hippo Video API, this operation is `GET /api/v1/me/video/reports/:video_id` (base URL `https://www.hippovideo.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-video-reports.md) for the provider-specific parameters and requirements.

