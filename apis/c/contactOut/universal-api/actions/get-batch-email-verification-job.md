# ContactOut: Get Batch Email Verification Job

Retrieves a batch email verification job from ContactOut.

```
GET https://connect.mindcloud.co/v1/universal/contactOut/latest/actions/get-batch-email-verification-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ContactOut `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/contactOut/latest/actions/get-batch-email-verification-job?connectionId=$CONNECTION_ID&job_uuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "job_uuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/contactOut/latest/actions/get-batch-email-verification-job?${params}`, {
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
| `job_uuid` | string | yes | The bulk email verification job identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Batch verification job status and result payload. |
| `message` | string | API response message. |

## Native endpoint

Through the native ContactOut API, this operation is `GET /v1/email/verify/batch/:job_uuid` (base URL `https://api.contactout.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-batch-email-verification-job.md) for the provider-specific parameters and requirements.

