# Opportify: Get IP Batch Status

Retrieves the status of an IP batch job in Opportify.

```
GET https://connect.mindcloud.co/v1/universal/opportify/latest/actions/get-ip-batch-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Opportify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/opportify/latest/actions/get-ip-batch-status?connectionId=$CONNECTION_ID&jobId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/opportify/latest/actions/get-ip-batch-status?${params}`, {
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
| `jobId` | string | yes | The unique identifier of the batch job to retrieve status for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "downloadUrls": {},
      "jobId": "string",
      "name": "Ava Chen",
      "progress": 1,
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
| `downloadUrls` | object | Available download URLs for the batch job results. Only present when status is "COMPLETED". |
| `jobId` | string | Unique identifier for the batch job. |
| `name` | string | Name of the batch job, if provided. |
| `progress` | number | Percentage of completion for the batch job (0-100). |
| `status` | string | Current status of the batch job. Allowed values: `QUEUED`, `PROCESSING`, `COMPLETED`, `ERROR`. Example: `COMPLETED`. |
| `statusDescription` | string | Description of the status, particularly useful when status is ERROR. |

## Native endpoint

Through the native Opportify API, this operation is `GET /ip/batch/:jobId` (base URL `https://api.opportify.ai/insights/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ip-batch-status.md) for the provider-specific parameters and requirements.

