# BHuman: Get Video Instance

Retrieves an AI Studio video instance from BHuman.

```
GET https://connect.mindcloud.co/v1/universal/bHuman/latest/actions/get-video-instance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BHuman `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bHuman/latest/actions/get-video-instance?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bHuman/latest/actions/get-video-instance?${params}`, {
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
| `id` | string | yes | The BHuman video instance ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "result": [
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
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `result[].actorId` | string |  |
| `result[].colorMode` | object |  |
| `result[].createdAt` | date |  |
| `result[].folderId` | string |  |
| `result[].greetings` | string |  |
| `result[].id` | string |  |
| `result[].industry` | number |  |
| `result[].mode` | number |  |
| `result[].name` | string |  |
| `result[].processedVideoId` | object |  |
| `result[].productId` | object |  |
| `result[].textToVideo` | boolean |  |
| `result[].thumbnail` | string |  |
| `result[].trainingUrl` | object |  |
| `result[].updatedAt` | date |  |
| `result[].useCase` | string |  |
| `result[].userId` | string |  |
| `result[].variableTimingConfig` | object |  |
| `result[].videoDistanceExecutionName` | object |  |
| `result[].videoDistanceStatus` | object |  |
| `result[].videoId` | string |  |
| `result[].videoPercentOfFace` | object |  |
| `result[].videosPreviewFlag` | object |  |
| `result[].voiceConfig` | object |  |

## Native endpoint

Through the native BHuman API, this operation is `GET /ai_studio/video_instance` (base URL `https://studio.bhuman.ai/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-video-instance.md) for the provider-specific parameters and requirements.

