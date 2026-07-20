# Opportify: Get IP Batch Export Status

Retrieves the status of an IP batch export job in Opportify.

```
GET https://connect.mindcloud.co/v1/universal/opportify/latest/actions/get-ip-batch-export-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Opportify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/opportify/latest/actions/get-ip-batch-export-status?connectionId=$CONNECTION_ID&jobId=string&exportId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "string",
  "exportId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/opportify/latest/actions/get-ip-batch-export-status?${params}`, {
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
| `jobId` | string | yes | The unique identifier of the batch job. Format: uuid. Example: "52b36b1f-0c21-41fa-8a4f-423d25a9a8e2". |
| `exportId` | string | yes | The unique identifier of the export job. Format: uuid. Example: "3b90d156-a0d8-4630-8230-f59e9a4e9e33". |

## Response

```json
{
  "success": true,
  "data": [
    {
      "columns": [
        "string"
      ],
      "downloadUrl": "https://example.com",
      "errorCode": "string",
      "errorMessage": "string",
      "expiresAt": "string",
      "exportId": "string",
      "filters": [
        {}
      ],
      "format": "string",
      "jobId": "string",
      "requestedAt": "string",
      "resultSizeBytes": 1,
      "status": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `columns` | array<string> | List of columns included in the export. |
| `downloadUrl` | string | Pre-signed URL to download the export file. Only present when status is `COMPLETED`. Format: uri. Example: "https://opportify-batch-analysis.s3.amazonaws.com/...". |
| `errorCode` | string | Error code if the export failed. Only present when status is `FAILED`. |
| `errorMessage` | string | Error message if the export failed. Only present when status is `FAILED`. |
| `expiresAt` | string | Expiration timestamp for the download URL (ISO 8601 format). Only present when status is `COMPLETED`. Format: date-time. Example: "2025-11-07T14:32:15.000Z". |
| `exportId` | string | The unique identifier for the export job. Format: uuid. Example: "6f8d88ef-0896-4f69-90cd-7cc6ce5e6ddf". |
| `filters` | array<object> | List of filters applied to the export. |
| `format` | string | The output format of the export. Allowed values: `csv`, `json`. Example: `csv`. |
| `jobId` | string | The batch job identifier. Format: uuid. Example: "84d22c8b-2cb6-4606-bfb1-361244a097e4". |
| `requestedAt` | string | Timestamp when the export was requested (ISO 8601 format). Format: date-time. Example: "2025-11-07T10:30:00.000Z". |
| `resultSizeBytes` | number | Size of the export file in bytes. Only present when status is `COMPLETED`. |
| `status` | string | Current status of the export job. Allowed values: `QUEUED`, `PROCESSING`, `COMPLETED`, `FAILED`. Example: `COMPLETED`. |
| `updatedAt` | string | Timestamp when the export status was last updated (ISO 8601 format). Format: date-time. Example: "2025-11-07T10:32:15.000Z". |

## Native endpoint

Through the native Opportify API, this operation is `GET /ip/batch/:jobId/exports/:exportId` (base URL `https://api.opportify.ai/insights/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ip-batch-export-status.md) for the provider-specific parameters and requirements.

