# Opportify: Batch Analyze Emails

Creates an asynchronous email analysis job in Opportify.

```
POST https://connect.mindcloud.co/v1/universal/opportify/latest/actions/batch-analyze-emails
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Opportify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/opportify/latest/actions/batch-analyze-emails" \
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
const response = await fetch('https://connect.mindcloud.co/v1/universal/opportify/latest/actions/batch-analyze-emails', {
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
| `emails[]` | array<string> | yes | Array of email addresses to analyze. |
| `name` | string | no | Optional name for the batch job. |
| `enableAI` | boolean | no | Enable AI-based analysis for insights. |
| `enableAutoCorrection` | boolean | no | Controls email auto-correction behavior for batch processing. Default: `false`. - When set to `true`: The system will automatically apply corrections when highly confident. The analysis will be performed on corrected email addresses. - When set to `false`: The system will still suggest corrections in the results, but the analysis will remain based on the original email addresses provided. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "jobId": "string",
      "name": "Ava Chen",
      "status": "string",
      "statusDescription": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `jobId` | string | Unique identifier for the batch job. |
| `name` | string | Name of the batch job, if provided. |
| `status` | string | Current status of the batch job. Allowed values: `QUEUED`, `PROCESSING`, `COMPLETED`, `ERROR`. Example: `QUEUED`. |
| `statusDescription` | string | Description of the status, particularly useful when status is ERROR. |

## Native endpoint

Through the native Opportify API, this operation is `POST /email/batch` (base URL `https://api.opportify.ai/insights/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/batch-analyze-emails.md) for the provider-specific parameters and requirements.

