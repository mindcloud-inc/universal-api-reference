# ClearBounce: Create Batch Verification Job

Creates a batch verification job in ClearBounce.

```
POST https://connect.mindcloud.co/v1/universal/clearBounce/latest/actions/create-batch-verification-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClearBounce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clearBounce/latest/actions/create-batch-verification-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "emails[]": [
    "ava@example.com"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clearBounce/latest/actions/create-batch-verification-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "emails[]": ["ava@example.com"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `emails[]` | array<string> | yes | Array of email addresses to verify in one batch request. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "duplicateCount": 1,
      "emptyRows": 1,
      "estimatedTimeSeconds": 1,
      "invalidRows": 1,
      "jobId": "string",
      "skippedRows": 1,
      "success": true,
      "totalEmails": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `duplicateCount` | number | Number of duplicate rows removed from the submitted payload. |
| `emptyRows` | number | Number of empty rows in the submitted batch payload. |
| `estimatedTimeSeconds` | number | Provider-estimated processing time for the batch job. |
| `invalidRows` | number | Number of invalid rows in the submitted batch payload. |
| `jobId` | string | The created ClearBounce batch verification job ID. |
| `skippedRows` | number | Number of skipped rows in the submitted batch payload. |
| `success` | boolean | Whether the batch upload request succeeded. |
| `totalEmails` | number | Number of emails accepted into the batch job. |

## Native endpoint

Through the native ClearBounce API, this operation is `POST /bulk/upload` (base URL `https://api.clearbounce.net/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-batch-verification-job.md) for the provider-specific parameters and requirements.

