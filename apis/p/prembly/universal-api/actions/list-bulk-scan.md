# Prembly: List Bulk Scan

Retrieves bulk fraud scans from Prembly.

```
GET https://connect.mindcloud.co/v1/universal/prembly/latest/actions/list-bulk-scan
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Prembly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/prembly/latest/actions/list-bulk-scan?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/prembly/latest/actions/list-bulk-scan?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "bulk_id": "string",
      "completed_at": "2026-05-07T12:00:00.000Z",
      "error_count": 1,
      "error_file_url": "https://example.com",
      "error_message": "string",
      "processed_records": 1,
      "result_file_url": "https://example.com",
      "scan_type": "string",
      "status": "string",
      "success_count": 1,
      "total_records": 1,
      "uploaded_at": "2026-05-07T12:00:00.000Z",
      "uploaded_by": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bulk_id` | string |  |
| `completed_at` | date |  |
| `error_count` | number |  |
| `error_file_url` | string |  |
| `error_message` | string |  |
| `processed_records` | number |  |
| `result_file_url` | string |  |
| `scan_type` | string |  |
| `status` | string |  |
| `success_count` | number |  |
| `total_records` | number |  |
| `uploaded_at` | date |  |
| `uploaded_by` | string |  |

## Native endpoint

Through the native Prembly API, this operation is `GET /api/v1/fraud/bulk-scan/` (base URL `https://api.prembly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-bulk-scan.md) for the provider-specific parameters and requirements.

