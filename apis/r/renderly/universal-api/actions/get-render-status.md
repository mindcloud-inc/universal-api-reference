# Renderly: Get Render Status

Retrieves a render job's status from Renderly.

```
GET https://connect.mindcloud.co/v1/universal/renderly/latest/actions/get-render-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Renderly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/renderly/latest/actions/get-render-status?connectionId=$CONNECTION_ID&jobId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/renderly/latest/actions/get-render-status?${params}`, {
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
| `jobId` | string | yes | The ID of the render job. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completedAt": "2026-05-07T12:00:00.000Z",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "creditsUsed": 1,
      "duration": 1,
      "durationInFrames": 1,
      "errorMessage": "string",
      "estimatedTimeRemaining": 1,
      "fps": 1,
      "height": 1,
      "jobId": "string",
      "outputSize": 1,
      "outputUrl": "https://example.com",
      "progressPercentage": 1,
      "project": {
        "id": "string",
        "name": "Ava Chen",
        "templateId": "string"
      },
      "projectId": "string",
      "status": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "width": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completedAt` | date |  |
| `createdAt` | date |  |
| `creditsUsed` | number |  |
| `duration` | number |  |
| `durationInFrames` | number |  |
| `errorMessage` | string |  |
| `estimatedTimeRemaining` | number |  |
| `fps` | number |  |
| `height` | number |  |
| `jobId` | string |  |
| `outputSize` | number |  |
| `outputUrl` | string |  |
| `progressPercentage` | number |  |
| `project` | object |  |
| `project.id` | string |  |
| `project.name` | string |  |
| `project.templateId` | string |  |
| `projectId` | string |  |
| `status` | string |  |
| `updatedAt` | date |  |
| `width` | number |  |

## Native endpoint

Through the native Renderly API, this operation is `GET /renders/:jobId` (base URL `https://renderly.video/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-render-status.md) for the provider-specific parameters and requirements.

