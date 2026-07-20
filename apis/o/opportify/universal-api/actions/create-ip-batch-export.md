# Opportify: Create IP Batch Export

Creates an export job for IP batch results in Opportify.

```
POST https://connect.mindcloud.co/v1/universal/opportify/latest/actions/create-ip-batch-export
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Opportify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/opportify/latest/actions/create-ip-batch-export" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "jobId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/opportify/latest/actions/create-ip-batch-export', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "jobId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `jobId` | string | yes | The unique identifier of the completed batch job. Format: uuid. Example: "52b36b1f-0c21-41fa-8a4f-423d25a9a8e2". |
| `exportType` | string | no | Output format for the export. If omitted, the server will use `csv` as the default format. Allowed values: `csv`, `json`. Example: `csv`. |
| `filters` | object | no | Field-level filters to apply to the export. Supports string filters (exact match, comma-separated, or arrays), numeric filters (exact values, arrays, or range objects with min/max), and nested field access using dot notation. - Maximum 25 filters - Maximum 50 values per filter |
| `columns[]` | array<string> | no | Array of field paths to include in the export. If omitted, all fields are included. Maximum 100 columns. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "exportId": "string",
      "jobId": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `exportId` | string | The unique identifier for the export job. Format: uuid. Example: "6f8d88ef-0896-4f69-90cd-7cc6ce5e6ddf". |
| `jobId` | string | The batch job identifier. Format: uuid. Example: "84d22c8b-2cb6-4606-bfb1-361244a097e4". |
| `status` | string | Initial status of the export job. Allowed value: `QUEUED`. Example: `QUEUED`. |

## Native endpoint

Through the native Opportify API, this operation is `POST /ip/batch/:jobId/exports` (base URL `https://api.opportify.ai/insights/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-ip-batch-export.md) for the provider-specific parameters and requirements.

