# Hippo Video: Generate Personalized Videos

Creates personalized videos in Hippo Video.

```
POST https://connect.mindcloud.co/v1/universal/hippoVideo/latest/actions/generate-personalized-videos
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hippo Video `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hippoVideo/latest/actions/generate-personalized-videos" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "videoId": 1,
  "mergeFields": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hippoVideo/latest/actions/generate-personalized-videos', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "videoId": 1,
    "mergeFields": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `videoId` | number | yes | ID of the video |
| `mergeFields` | string | yes | JSON array of merge field values |

## Response

```json
{
  "success": true,
  "data": [
    {
      "personalizedVideos": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `personalizedVideos[]` | array<object> |  |
| `personalizedVideos[].payload` | object |  |
| `personalizedVideos[].payload.company` | string |  |
| `personalizedVideos[].payload.embedUrl` | string |  |
| `personalizedVideos[].payload.firstName` | string |  |
| `personalizedVideos[].payload.shareUrl` | string |  |
| `personalizedVideos[].payload.thumbnailUrl` | string |  |

## Native endpoint

Through the native Hippo Video API, this operation is `POST /api/v1/me/video/personalize` (base URL `https://www.hippovideo.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-personalized-videos.md) for the provider-specific parameters and requirements.

