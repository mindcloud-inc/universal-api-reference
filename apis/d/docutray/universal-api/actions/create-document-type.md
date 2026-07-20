# Docutray: Create Document Type



```
POST https://connect.mindcloud.co/v1/universal/docutray/latest/actions/create-document-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docutray `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docutray/latest/actions/create-document-type" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "codeType": "string",
  "description": "string",
  "jsonSchema": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docutray/latest/actions/create-document-type', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "codeType": "string",
    "description": "string",
    "jsonSchema": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Document type name |
| `codeType` | string | yes | Unique code identifier |
| `description` | string | yes | Document type description |
| `jsonSchema` | object | yes | JSON Schema for document validation |
| `isDraft` | boolean | no | Whether the document type is a draft |
| `promptHints` | string | no | Hints for the OCR prompt |
| `identifyPromptHints` | string | no | Hints for the document identification prompt |
| `conversionMode` | string | no | Conversion mode |
| `keepPropertyOrdering` | boolean | no | Whether to preserve property ordering in schema |
| `isPublic` | boolean | no | Whether the document type is public |

## Response

```json
{
  "success": true,
  "data": [
    {
      "codeType": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": "string",
      "isDraft": true,
      "isPublic": true,
      "name": "Ava Chen",
      "status": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `codeType` | string |  |
| `createdAt` | date |  |
| `description` | string |  |
| `id` | string |  |
| `isDraft` | boolean |  |
| `isPublic` | boolean |  |
| `name` | string |  |
| `status` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Docutray API, this operation is `POST api/document-types` (base URL `https://app.docutray.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-document-type.md) for the provider-specific parameters and requirements.

