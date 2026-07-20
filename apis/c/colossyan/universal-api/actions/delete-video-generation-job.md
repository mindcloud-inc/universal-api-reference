# Colossyan: Delete Video Generation Job

Deletes a video generation job from Colossyan.

```
DELETE https://connect.mindcloud.co/v1/universal/colossyan/latest/actions/delete-video-generation-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Colossyan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/colossyan/latest/actions/delete-video-generation-job?connectionId=$CONNECTION_ID&videoGenerationJobId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "videoGenerationJobId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/colossyan/latest/actions/delete-video-generation-job?${params}`, {
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
| `videoGenerationJobId` | string | yes | ID of the video generation job to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Deletion confirmation message from Colossyan. |

## Native endpoint

Through the native Colossyan API, this operation is `DELETE /video-generation-jobs/:videoGenerationJobId` (base URL `https://app.colossyan.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-video-generation-job.md) for the provider-specific parameters and requirements.

