# Xodo Sign: List Bulk Job Documents

Retrieves documents from a bulk job in Xodo Sign.

```
GET https://connect.mindcloud.co/v1/universal/xodoSign/latest/actions/list-bulk-job-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Xodo Sign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xodoSign/latest/actions/list-bulk-job-documents?connectionId=$CONNECTION_ID&bulkSendingJobId=1&business_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "bulkSendingJobId": "1",
  "business_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xodoSign/latest/actions/list-bulk-job-documents?${params}`, {
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
| `bulkSendingJobId` | number | yes | The bulk sending job ID to retrieve documents for. |
| `business_id` | string | yes | The Xodo Sign business ID that owns the bulk job. |
| `limit` | number | no | Maximum amount of documents to fetch. |
| `offset` | number | no | Number of documents to skip when fetching results. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "pagination": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Documents created by the selected bulk job. |
| `pagination` | object | Pagination metadata for the bulk job documents result set. |

## Native endpoint

Through the native Xodo Sign API, this operation is `GET /bulk_job/:bulkSendingJobId/documents` (base URL `https://api.eversign.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-bulk-job-documents.md) for the provider-specific parameters and requirements.

