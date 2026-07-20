# Enrich.so: Get Batch Finder Results

Retrieves batch email finder results from Enrich.so.

```
GET https://connect.mindcloud.co/v1/universal/enrich/latest/actions/get-batch-finder-results
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Enrich.so `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/enrich/latest/actions/get-batch-finder-results?connectionId=$CONNECTION_ID&limit=25&offset=0&batchId=665a1f4e2c3b7800129dce01" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "batchId": "665a1f4e2c3b7800129dce01"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/enrich/latest/actions/get-batch-finder-results?${params}`, {
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
| `batchId` | string | yes | Batch ID returned by the batch email finder submit action. Default: `665a1f4e2c3b7800129dce01`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "batchId": "string",
      "confidence": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "lastName": "Chen",
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
| `batchId` | string | Email finder batch identifier. |
| `confidence` | string | Confidence for the resolved email. |
| `email` | string | Resolved email on an individual result. |
| `firstName` | string | Lead first name. |
| `lastName` | string | Lead last name. |
| `processedCount` | number | Leads processed in the batch. |
| `results` | array<object> | Email finder result objects for the page. |
| `status` | string | Final or current batch status. |
| `totalItems` | number | Total leads in the batch. |

## Native endpoint

Through the native Enrich.so API, this operation is `GET /email-finder/batch/{batchId}/results` (base URL `https://dev.enrich.so/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-batch-finder-results.md) for the provider-specific parameters and requirements.

