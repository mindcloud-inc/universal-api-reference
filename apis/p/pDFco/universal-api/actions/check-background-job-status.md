# PDF.co: Check Background Job Status

Retrieves a background job status from PDF.co.

```
GET https://connect.mindcloud.co/v1/universal/pDFco/latest/actions/check-background-job-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PDF.co `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pDFco/latest/actions/check-background-job-status?connectionId=$CONNECTION_ID&jobid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pDFco/latest/actions/check-background-job-status?${params}`, {
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
| `jobid` | string | yes | Background job identifier returned by async PDF.co endpoints. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "credits": 1,
      "duration": 1,
      "jobDuration": 1,
      "jobId": "string",
      "message": "string",
      "outputLinkValidTill": "https://example.com",
      "pageCount": 1,
      "remainingCredits": 1,
      "status": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `credits` | number |  |
| `duration` | number |  |
| `jobDuration` | number |  |
| `jobId` | string |  |
| `message` | string |  |
| `outputLinkValidTill` | string |  |
| `pageCount` | number |  |
| `remainingCredits` | number |  |
| `status` | string |  |
| `url` | string |  |

## Native endpoint

Through the native PDF.co API, this operation is `GET /job/check` (base URL `https://api.pdf.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-background-job-status.md) for the provider-specific parameters and requirements.

