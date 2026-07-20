# EndBounce: Get Verification Job Status

Retrieves a verification job status from EndBounce.

```
GET https://connect.mindcloud.co/v1/universal/endBounce/latest/actions/get-verification-job-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EndBounce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/endBounce/latest/actions/get-verification-job-status?connectionId=$CONNECTION_ID&request_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "request_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/endBounce/latest/actions/get-verification-job-status?${params}`, {
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
| `request_id` | string | yes | Verification job request ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "acceptAll": 1,
      "fileName": "Ava Chen",
      "invalid": 1,
      "processed": 1,
      "requestId": "string",
      "risky": 1,
      "status": "string",
      "total": 1,
      "uploadedAt": "2026-05-07T12:00:00.000Z",
      "valid": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `acceptAll` | number | Accept-all rows counted so far. |
| `fileName` | string | Display name for the verification job. |
| `invalid` | number | Invalid rows counted so far. |
| `processed` | number | Rows processed so far. |
| `requestId` | string | Verification job request ID. |
| `risky` | number | Risky rows counted so far. |
| `status` | string | Current job status. |
| `total` | number | Total rows in the job. |
| `uploadedAt` | date | When the job was submitted. |
| `valid` | number | Valid rows counted so far. |

## Native endpoint

Through the native EndBounce API, this operation is `GET /v1/jobs/:request_id/status` (base URL `https://api.endbounce.com/api/integrations`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-verification-job-status.md) for the provider-specific parameters and requirements.

