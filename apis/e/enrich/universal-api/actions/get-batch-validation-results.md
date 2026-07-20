# Enrich.so: Get Batch Validation Results

Retrieves batch email validation results from Enrich.so.

```
GET https://connect.mindcloud.co/v1/universal/enrich/latest/actions/get-batch-validation-results
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Enrich.so `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/enrich/latest/actions/get-batch-validation-results?connectionId=$CONNECTION_ID&limit=25&offset=0&batchId=665a1f4e2c3b7800129dce01" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "batchId": "665a1f4e2c3b7800129dce01"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/enrich/latest/actions/get-batch-validation-results?${params}`, {
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
| `batchId` | string | yes | Batch ID returned by the batch validation submit action. Default: `665a1f4e2c3b7800129dce01`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "batchId": "string",
      "confidence": "string",
      "email": "ava@example.com",
      "processedCount": 1,
      "result": "string",
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
| `batchId` | string | Batch identifier. |
| `confidence` | string | Validation confidence for an individual result. |
| `email` | string | Email address on an individual validation result. |
| `processedCount` | number | Emails processed in the batch. |
| `result` | string | Validation result for an individual email. |
| `results` | array<object> | Validation result objects for the page. |
| `status` | string | Final or current batch status. |
| `totalItems` | number | Total emails in the batch. |

## Native endpoint

Through the native Enrich.so API, this operation is `GET /email-validation/batch/{batchId}/results` (base URL `https://dev.enrich.so/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-batch-validation-results.md) for the provider-specific parameters and requirements.

