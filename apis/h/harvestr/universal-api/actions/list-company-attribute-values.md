# Harvestr.io: List Company Attribute Values



```
GET https://connect.mindcloud.co/v1/universal/harvestr/latest/actions/list-company-attribute-values
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Harvestr.io `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/harvestr/latest/actions/list-company-attribute-values?connectionId=$CONNECTION_ID&limit=25&offset=0&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/harvestr/latest/actions/list-company-attribute-values?${params}`, {
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
| `id` | string | yes | Unique identifier (id or clientId) |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `createdBefore` | date | no | Filter items created before this date (ISO 8601 format) |
| `createdAfter` | date | no | Filter items created after this date (ISO 8601 format) |
| `updatedBefore` | date | no | Filter items updated before this date (ISO 8601 format) |
| `updatedAfter` | date | no | Filter items updated after this date (ISO 8601 format) |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributeId": "string",
      "booleanValue": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "dateValue": "string",
      "numericValue": 1,
      "ratingValue": 1,
      "textValue": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "urlValue": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributeId` | string | Identifier of the associated attribute |
| `booleanValue` | boolean | Boolean value (for BOOLEAN type attributes) |
| `createdAt` | date | Creation date of the attribute value |
| `dateValue` | string | Date value (for DATE type attributes) |
| `numericValue` | number | Numeric value (for NUMERIC type attributes) |
| `ratingValue` | number | Rating value (for RATING type attributes) |
| `textValue` | string | Text value (for TEXT type attributes) |
| `updatedAt` | date | Last update date of the attribute value |
| `urlValue` | string | URL value (for URL type attributes) |

## Native endpoint

Through the native Harvestr.io API, this operation is `GET /company/{id}/attribute-value` (base URL `https://rest.harvestr.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-company-attribute-values.md) for the provider-specific parameters and requirements.

