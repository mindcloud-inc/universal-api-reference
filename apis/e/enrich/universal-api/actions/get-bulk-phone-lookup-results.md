# Enrich.so: Get Bulk Phone Lookup Results

Retrieves bulk phone lookup results from Enrich.so.

```
GET https://connect.mindcloud.co/v1/universal/enrich/latest/actions/get-bulk-phone-lookup-results
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Enrich.so `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/enrich/latest/actions/get-bulk-phone-lookup-results?connectionId=$CONNECTION_ID&limit=25&offset=0&jobId=665a1f4e2c3b7800129dce02" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "jobId": "665a1f4e2c3b7800129dce02"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/enrich/latest/actions/get-bulk-phone-lookup-results?${params}`, {
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
| `jobId` | string | yes | Bulk phone lookup job ID. Default: `665a1f4e2c3b7800129dce02`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "jobId": "string",
      "linkedin": "https://example.com",
      "phones": [
        {}
      ],
      "processedCount": 1,
      "results": [
        {}
      ],
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
| `email` | string | Email associated with an individual phone lookup result. |
| `jobId` | string | Bulk phone lookup job identifier. |
| `linkedin` | string | LinkedIn profile URL for an individual result. |
| `phones` | array<object> | Phone records on an individual result. |
| `processedCount` | number | Lookup items processed in the job. |
| `results` | array<object> | Phone lookup result objects for the page. |
| `status` | string | Final or current job status. |
| `totalItems` | number | Total lookup items in the job. |

## Native endpoint

Through the native Enrich.so API, this operation is `GET /reverse-lookup/phones/bulk/{jobId}/results` (base URL `https://dev.enrich.so/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-bulk-phone-lookup-results.md) for the provider-specific parameters and requirements.

