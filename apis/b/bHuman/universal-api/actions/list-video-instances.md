# BHuman: List Video Instances

Retrieves AI Studio video instances from BHuman.

```
GET https://connect.mindcloud.co/v1/universal/bHuman/latest/actions/list-video-instances
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BHuman `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bHuman/latest/actions/list-video-instances?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bHuman/latest/actions/list-video-instances?${params}`, {
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
      "code": 1,
      "result": {
        "instances": [
          {
            "actorId": "string",
            "colorMode": {},
            "createdAt": "2026-05-07T12:00:00.000Z",
            "folderId": "string",
            "greetings": "string",
            "id": "string",
            "industry": 1,
            "mode": 1,
            "name": "Ava Chen",
            "processedVideoId": {},
            "productId": {},
            "textToVideo": true,
            "thumbnail": "string",
            "trainingUrl": {},
            "updatedAt": "2026-05-07T12:00:00.000Z",
            "useCase": "string",
            "userId": "string",
            "variableTimingConfig": {},
            "videoDistanceExecutionName": {},
            "videoDistanceStatus": {},
            "videoId": "string",
            "videoPercentOfFace": {},
            "videosPreviewFlag": {},
            "voiceConfig": {}
          }
        ],
        "total": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `result.instances[].actorId` | string |  |
| `result.instances[].colorMode` | object |  |
| `result.instances[].createdAt` | date |  |
| `result.instances[].folderId` | string |  |
| `result.instances[].greetings` | string |  |
| `result.instances[].id` | string |  |
| `result.instances[].industry` | number |  |
| `result.instances[].mode` | number |  |
| `result.instances[].name` | string |  |
| `result.instances[].processedVideoId` | object |  |
| `result.instances[].productId` | object |  |
| `result.instances[].textToVideo` | boolean |  |
| `result.instances[].thumbnail` | string |  |
| `result.instances[].trainingUrl` | object |  |
| `result.instances[].updatedAt` | date |  |
| `result.instances[].useCase` | string |  |
| `result.instances[].userId` | string |  |
| `result.instances[].variableTimingConfig` | object |  |
| `result.instances[].videoDistanceExecutionName` | object |  |
| `result.instances[].videoDistanceStatus` | object |  |
| `result.instances[].videoId` | string |  |
| `result.instances[].videoPercentOfFace` | object |  |
| `result.instances[].videosPreviewFlag` | object |  |
| `result.instances[].voiceConfig` | object |  |
| `result.total` | number |  |

## Native endpoint

Through the native BHuman API, this operation is `GET /ai_studio/video_instances` (base URL `https://studio.bhuman.ai/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-video-instances.md) for the provider-specific parameters and requirements.

