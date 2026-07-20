# Enrich.so: Check Bulk Phone Lookup Progress

Retrieves bulk phone lookup progress from Enrich.so.

```
GET https://connect.mindcloud.co/v1/universal/enrich/latest/actions/check-bulk-phone-lookup-progress
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Enrich.so `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/enrich/latest/actions/check-bulk-phone-lookup-progress?connectionId=$CONNECTION_ID&jobId=665a1f4e2c3b7800129dce02" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "665a1f4e2c3b7800129dce02"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/enrich/latest/actions/check-bulk-phone-lookup-progress?${params}`, {
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
      "jobId": "string",
      "processedItems": 1,
      "progress": 1,
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
| `jobId` | string | Bulk phone lookup job identifier. |
| `processedItems` | number | Items processed so far. |
| `progress` | number | Completion percentage from 0 to 100. |
| `status` | string | Current job status. |
| `totalItems` | number | Total items in the job. |

## Native endpoint

Through the native Enrich.so API, this operation is `GET /reverse-lookup/phones/bulk/{jobId}` (base URL `https://dev.enrich.so/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-bulk-phone-lookup-progress.md) for the provider-specific parameters and requirements.

