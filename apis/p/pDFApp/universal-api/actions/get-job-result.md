# PDF-app: Get Job Result

Retrieves an async job result from PDF-app.

```
GET https://connect.mindcloud.co/v1/universal/pDFApp/latest/actions/get-job-result
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PDF-app `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pDFApp/latest/actions/get-job-result?connectionId=$CONNECTION_ID&jobId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pDFApp/latest/actions/get-job-result?${params}`, {
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
| `jobId` | string | yes | The asynchronous job ID to look up. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Created_date": "string",
      "CreditzConsumed": 1,
      "extraction_results": [
        "string"
      ],
      "job_id": "string",
      "message": "string",
      "status": "string",
      "statusCode": 1,
      "URLs": [
        "https://example.com"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Created_date` | string |  |
| `CreditzConsumed` | number |  |
| `extraction_results` | array |  |
| `job_id` | string |  |
| `message` | string |  |
| `status` | string |  |
| `statusCode` | number |  |
| `URLs` | array<string> |  |

## Native endpoint

Through the native PDF-app API, this operation is `GET /async_jobid_check` (base URL `https://api.pdf-app.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-job-result.md) for the provider-specific parameters and requirements.

