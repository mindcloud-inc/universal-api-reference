# MailFloss: Get Batch Verification Status

Retrieves batch email verification job status from MailFloss.

```
GET https://connect.mindcloud.co/v1/universal/mailFloss/latest/actions/get-batch-verification-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailFloss `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailFloss/latest/actions/get-batch-verification-status?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailFloss/latest/actions/get-batch-verification-status?${params}`, {
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
| `id` | string | yes | Batch verification job ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "emailsProcessed": 1,
      "id": "string",
      "numFailed": 1,
      "numImported": 1,
      "numPassed": 1,
      "numRisky": 1,
      "numUndeliverable": 1,
      "numUnknown": 1,
      "processed": true,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `emailsProcessed` | number | Number of email addresses processed. |
| `id` | string | Batch verification job ID. |
| `numFailed` | number | Number of email addresses that failed verification. |
| `numImported` | number | Number of email addresses imported. |
| `numPassed` | number | Number of valid email addresses. |
| `numRisky` | number | Number of risky email addresses. |
| `numUndeliverable` | number | Number of undeliverable email addresses. |
| `numUnknown` | number | Number of unknown email addresses. |
| `processed` | boolean | Whether the job has finished processing. |
| `status` | string | Batch job status. |

## Native endpoint

Through the native MailFloss API, this operation is `GET /batch-verify/:id/status` (base URL `https://api.mailfloss.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-batch-verification-status.md) for the provider-specific parameters and requirements.

