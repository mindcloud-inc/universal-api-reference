# Colossyan: Retrieve Video Generation Job

Retrieves a video generation job from Colossyan.

```
GET https://connect.mindcloud.co/v1/universal/colossyan/latest/actions/retrieve-video-generation-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Colossyan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/colossyan/latest/actions/retrieve-video-generation-job?connectionId=$CONNECTION_ID&videoGenerationJobId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "videoGenerationJobId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/colossyan/latest/actions/retrieve-video-generation-job?${params}`, {
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
| `videoGenerationJobId` | string | yes | ID of the video generation job to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creationDate": "string",
      "folderId": "string",
      "id": "string",
      "isAPIGenerated": true,
      "maximumProgress": 1,
      "progress": 1,
      "sharded": true,
      "status": "string",
      "userId": "string",
      "videoCreative": {},
      "videoId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creationDate` | string | ISO timestamp when the video generation job was created. |
| `folderId` | string | Folder ID containing the job when present. |
| `id` | string | Colossyan video generation job ID. |
| `isAPIGenerated` | boolean | Whether the job was created through the API. |
| `maximumProgress` | number | Maximum progress value for the job lifecycle. |
| `progress` | number | Current job progress value. |
| `sharded` | boolean | Whether the job is sharded internally by Colossyan. |
| `status` | string | Current job status. |
| `userId` | string | Workspace user ID that owns the job. |
| `videoCreative` | object | Nested video creative payload used to generate the job. |
| `videoId` | string | Generated video ID created by the job. |

## Native endpoint

Through the native Colossyan API, this operation is `GET /video-generation-jobs/:videoGenerationJobId` (base URL `https://app.colossyan.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-video-generation-job.md) for the provider-specific parameters and requirements.

