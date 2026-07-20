# Enrich.so: Get Bulk Lookup Results

Retrieves bulk profile lookup results from Enrich.so.

```
GET https://connect.mindcloud.co/v1/universal/enrich/latest/actions/get-bulk-lookup-results
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Enrich.so `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/enrich/latest/actions/get-bulk-lookup-results?connectionId=$CONNECTION_ID&limit=25&offset=0&batchId=665a1f4e2c3b7800129dce03" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "batchId": "665a1f4e2c3b7800129dce03"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/enrich/latest/actions/get-bulk-lookup-results?${params}`, {
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
| `batchId` | string | yes | Bulk reverse lookup batch ID. Default: `665a1f4e2c3b7800129dce03`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "batchId": "string",
      "company": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "lastName": "Chen",
      "processedCount": 1,
      "results": [
        {}
      ],
      "status": "string",
      "title": "string",
      "totalItems": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `batchId` | string | Bulk reverse lookup batch identifier. |
| `company` | string | Person company name. |
| `email` | string | Email address on an individual profile result. |
| `firstName` | string | Person first name. |
| `lastName` | string | Person last name. |
| `processedCount` | number | Emails processed in the batch. |
| `results` | array<object> | Professional profile result objects for the page. |
| `status` | string | Final or current batch status. |
| `title` | string | Person job title. |
| `totalItems` | number | Total emails in the batch. |

## Native endpoint

Through the native Enrich.so API, this operation is `GET /reverse-lookup/bulk-lookup/{batchId}/results` (base URL `https://dev.enrich.so/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-bulk-lookup-results.md) for the provider-specific parameters and requirements.

