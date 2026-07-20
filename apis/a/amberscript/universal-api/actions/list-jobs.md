# Amberscript: List Jobs

Retrieves jobs from your Amberscript account.

```
GET https://connect.mindcloud.co/v1/universal/amberscript/latest/actions/list-jobs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Amberscript `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/amberscript/latest/actions/list-jobs?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/amberscript/latest/actions/list-jobs?${params}`, {
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
| `jobId` | string | no | Return only the job with this ID. |
| `jobType` | string | no | Filter jobs by type, such as `perfect` or `direct`. |
| `status` | string | no | Filter jobs by status: `OPEN`, `ERROR`, or `DONE`. |
| `transcriptionType` | string | no | Filter jobs by transcription type, such as `transcription`. |

## Response

```json
{
  "success": true,
  "data": [
    {
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
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date |  |
| `filename` | string |  |
| `jobId` | string |  |
| `jobOptions.anonymization` | string |  |
| `jobOptions.burnInSubtitles` | boolean |  |
| `jobOptions.dresingPehl` | boolean |  |
| `jobOptions.extendedDelivery` | string |  |
| `jobOptions.portal` | boolean |  |
| `jobOptions.timestampEnabledInExport` | boolean |  |
| `jobType` | string |  |
| `language` | string |  |
| `nrAudioSeconds` | number |  |
| `status` | string |  |
| `transcriptionType` | string |  |

## Native endpoint

Through the native Amberscript API, this operation is `GET /jobs` (base URL `https://api.amberscript.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-jobs.md) for the provider-specific parameters and requirements.

