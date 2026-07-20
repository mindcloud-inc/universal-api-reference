# Docutray: Update Document Type



```
PUT https://connect.mindcloud.co/v1/universal/docutray/latest/actions/update-document-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docutray `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/docutray/latest/actions/update-document-type" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docutray/latest/actions/update-document-type', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Document type ID |
| `name` | string | no | Document type name |
| `description` | string | no | Document type description |
| `jsonSchema` | object | no | JSON Schema for document validation |
| `isDraft` | boolean | no | Whether the document type is a draft |
| `promptHints` | string | no | Hints for the OCR prompt |
| `identifyPromptHints` | string | no | Hints for the document identification prompt |
| `conversionMode` | string | no | Conversion mode |
| `keepPropertyOrdering` | boolean | no | Whether to preserve property ordering in schema |
| `isPublic` | boolean | no | Whether the document type is public |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Docutray API returns.

## Native endpoint

Through the native Docutray API, this operation is `PUT api/document-types/:id` (base URL `https://app.docutray.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-document-type.md) for the provider-specific parameters and requirements.

