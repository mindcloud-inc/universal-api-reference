# Harvestr.io: Update Company Attribute Values



```
PUT https://connect.mindcloud.co/v1/universal/harvestr/latest/actions/update-company-attribute-values
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Harvestr.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/harvestr/latest/actions/update-company-attribute-values" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "attributeId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/harvestr/latest/actions/update-company-attribute-values', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "attributeId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Unique identifier (id or clientId) |
| `attributeId` | string | yes | ID of the attribute to retrieve for the company |
| `textValue` | string | no | Required for TEXT attribute |
| `numericValue` | number | no | Required for NUMERIC attribute |
| `booleanValue` | boolean | no | Required for BOOLEAN attribute |
| `dateValue` | string | no | Required for DATE attribute |
| `urlValue` | string | no | Required for URL attribute |
| `ratingValue` | string | no | Required for RATING attribute |

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

Through the native Harvestr.io API, this operation is `PATCH /company/{id}/attribute/{attributeId}` (base URL `https://rest.harvestr.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-company-attribute-values.md) for the provider-specific parameters and requirements.

