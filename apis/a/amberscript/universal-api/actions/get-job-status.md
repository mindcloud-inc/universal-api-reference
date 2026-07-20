# Amberscript: Get Job Status

Retrieves the status of an Amberscript job.

```
GET https://connect.mindcloud.co/v1/universal/amberscript/latest/actions/get-job-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Amberscript `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/amberscript/latest/actions/get-job-status?connectionId=$CONNECTION_ID&jobId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/amberscript/latest/actions/get-job-status?${params}`, {
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
| `jobId` | string | yes | The job to inspect. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "jobStatus": {
        "created": "2026-05-07T12:00:00.000Z",
        "filename": "Ava Chen",
        "jobId": "string",
        "jobOptions": {
          "anonymization": "string",
          "burnInSubtitles": true,
          "dresingPehl": true,
          "extendedDelivery": "string",
          "portal": true,
          "timestampEnabledInExport": true
        },
        "jobType": "string",
        "language": "string",
        "nrAudioSeconds": 1,
        "status": "string",
        "transcriptionType": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `jobStatus.created` | date |  |
| `jobStatus.filename` | string |  |
| `jobStatus.jobId` | string |  |
| `jobStatus.jobOptions.anonymization` | string |  |
| `jobStatus.jobOptions.burnInSubtitles` | boolean |  |
| `jobStatus.jobOptions.dresingPehl` | boolean |  |
| `jobStatus.jobOptions.extendedDelivery` | string |  |
| `jobStatus.jobOptions.portal` | boolean |  |
| `jobStatus.jobOptions.timestampEnabledInExport` | boolean |  |
| `jobStatus.jobType` | string |  |
| `jobStatus.language` | string |  |
| `jobStatus.nrAudioSeconds` | number |  |
| `jobStatus.status` | string |  |
| `jobStatus.transcriptionType` | string |  |

## Native endpoint

Through the native Amberscript API, this operation is `GET /jobs/status` (base URL `https://api.amberscript.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-job-status.md) for the provider-specific parameters and requirements.

