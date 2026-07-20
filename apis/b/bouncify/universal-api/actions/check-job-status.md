# Bouncify: Check Job Status

Retrieves bulk email list job status from Bouncify.

```
GET https://connect.mindcloud.co/v1/universal/bouncify/latest/actions/check-job-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bouncify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bouncify/latest/actions/check-job-status?connectionId=$CONNECTION_ID&jobId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bouncify/latest/actions/check-job-status?${params}`, {
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
| `jobId` | string | yes | Bulk verification job id to inspect. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "analysis": {
        "commonIsp": 1,
        "disposable": 1,
        "roleBased": 1,
        "spamtrap": 1,
        "syntaxError": 1
      },
      "createdAt": "string",
      "jobId": "string",
      "message": "string",
      "pending": 1,
      "results": {
        "acceptAll": 1,
        "deliverable": 1,
        "undeliverable": 1,
        "unknown": 1
      },
      "status": "string",
      "success": true,
      "total": 1,
      "verified": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `analysis.commonIsp` | number | Count of common ISP emails in the batch. |
| `analysis.disposable` | number | Count of disposable emails in the batch. |
| `analysis.roleBased` | number | Count of role-based emails in the batch. |
| `analysis.spamtrap` | number | Count of spamtrap emails in the batch. |
| `analysis.syntaxError` | number | Count of syntax-error emails in the batch. |
| `createdAt` | string | Timestamp when the job was created. |
| `jobId` | string | Bulk verification job identifier. |
| `message` | string | Provider message describing the status result. |
| `pending` | number | Number of pending emails when present. |
| `results.acceptAll` | number | Count of accept-all results when present. |
| `results.deliverable` | number | Count of deliverable results when present. |
| `results.undeliverable` | number | Count of undeliverable results when present. |
| `results.unknown` | number | Count of unknown results when present. |
| `status` | string | Current Bouncify status for the bulk job. |
| `success` | boolean | Whether the status request succeeded. |
| `total` | number | Total number of emails in the bulk job. |
| `verified` | number | Number of verified emails when present. |

## Native endpoint

Through the native Bouncify API, this operation is `GET /bulk/:job_id` (base URL `https://api.bouncify.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-job-status.md) for the provider-specific parameters and requirements.

