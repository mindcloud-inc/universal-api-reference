# Colossyan: Create Video Generation Job

Creates a new video generation job in Colossyan.

```
POST https://connect.mindcloud.co/v1/universal/colossyan/latest/actions/create-video-generation-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Colossyan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/colossyan/latest/actions/create-video-generation-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "videoCreative": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/colossyan/latest/actions/create-video-generation-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "videoCreative": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `videoCreative` | object | yes | Full Colossyan videoCreative object describing settings and scenes. |
| `dynamicVariables` | object | no | Optional dynamic variables object used by the video job. |
| `callback` | string | no | Optional callback URL for job completion events. |
| `callbackPayload` | object | no | Optional callback payload object. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "videoId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Created Colossyan video generation job ID. |
| `videoId` | string | Generated video ID associated with the created job. |

## Native endpoint

Through the native Colossyan API, this operation is `POST /video-generation-jobs` (base URL `https://app.colossyan.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-video-generation-job.md) for the provider-specific parameters and requirements.

