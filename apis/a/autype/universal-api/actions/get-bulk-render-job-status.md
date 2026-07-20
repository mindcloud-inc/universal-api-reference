# Autype: Get Bulk Render Job Status

Retrieves bulk render job status from Autype.

```
GET https://connect.mindcloud.co/v1/universal/autype/latest/actions/get-bulk-render-job-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Autype `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/autype/latest/actions/get-bulk-render-job-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/autype/latest/actions/get-bulk-render-job-status?${params}`, {
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
      "bulkJobId": "string",
      "completedAt": "2026-05-07T12:00:00.000Z",
      "completedItems": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "downloadUrl": "https://example.com",
      "error": "string",
      "failedItems": 1,
      "format": "string",
      "status": "string",
      "totalItems": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bulkJobId` | string |  |
| `completedAt` | date |  |
| `completedItems` | number |  |
| `createdAt` | date |  |
| `downloadUrl` | string |  |
| `error` | string |  |
| `failedItems` | number |  |
| `format` | string |  |
| `status` | string |  |
| `totalItems` | number |  |

## Native endpoint

Through the native Autype API, this operation is `GET /bulk-render/{bulkJobId}` (base URL `https://api.autype.com/api/v1/dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-bulk-render-job-status.md) for the provider-specific parameters and requirements.

