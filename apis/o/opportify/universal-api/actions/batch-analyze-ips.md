# Opportify: Batch Analyze IPs

Creates an asynchronous IP analysis job in Opportify.

```
POST https://connect.mindcloud.co/v1/universal/opportify/latest/actions/batch-analyze-ips
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Opportify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/opportify/latest/actions/batch-analyze-ips" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "ips[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/opportify/latest/actions/batch-analyze-ips', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "ips[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ips[]` | array<string> | yes | Array of IP addresses to analyze. |
| `name` | string | no | Optional name for the batch job. |
| `enableAI` | boolean | no | Enable AI-based analysis for insights. |

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

Through the native Opportify API, this operation is `POST /ip/batch` (base URL `https://api.opportify.ai/insights/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/batch-analyze-ips.md) for the provider-specific parameters and requirements.

