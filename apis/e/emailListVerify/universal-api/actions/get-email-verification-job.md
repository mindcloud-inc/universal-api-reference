# EmailListVerify: Get Email Verification Job

Retrieves email verification job status and results from EmailListVerify.

```
GET https://connect.mindcloud.co/v1/universal/emailListVerify/latest/actions/get-email-verification-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EmailListVerify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emailListVerify/latest/actions/get-email-verification-job?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/emailListVerify/latest/actions/get-email-verification-job?${params}`, {
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
| `id` | string | yes | Email verification job ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "finishedAt": "2026-05-07T12:00:00.000Z",
      "hasGreylist": true,
      "id": "string",
      "quality": "string",
      "result": {
        "email": "ava@example.com",
        "result": "string"
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | Creation timestamp. |
| `email` | string | Email being verified. |
| `finishedAt` | date | Completion timestamp. |
| `hasGreylist` | boolean | Whether greylisting is delaying verification. |
| `id` | string | Email verification job ID. |
| `quality` | string | Verification quality. |
| `result` | object | Detailed verification result when finished. |
| `result.email` | string | Verified email. |
| `result.result` | string | Deliverability status. |
| `status` | string | Job status. |

## Native endpoint

Through the native EmailListVerify API, this operation is `GET /api/emailJobs/:id` (base URL `https://api.emaillistverify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-email-verification-job.md) for the provider-specific parameters and requirements.

