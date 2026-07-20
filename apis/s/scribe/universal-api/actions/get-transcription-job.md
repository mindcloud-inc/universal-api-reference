# 3Scribe: Get Transcription Job

Retrieves a transcription job from 3Scribe.

```
GET https://connect.mindcloud.co/v1/universal/scribe/latest/actions/get-transcription-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 3Scribe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scribe/latest/actions/get-transcription-job?connectionId=$CONNECTION_ID&jobId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scribe/latest/actions/get-transcription-job?${params}`, {
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
| `jobId` | string | yes | The unique identifying code for the transcription job. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native 3Scribe API returns.

## Native endpoint

Through the native 3Scribe API, this operation is `GET /jobs/:jobid` (base URL `https://api.3scri.be`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-transcription-job.md) for the provider-specific parameters and requirements.

