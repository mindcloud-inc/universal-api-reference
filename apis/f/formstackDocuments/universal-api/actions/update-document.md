# Formstack Documents: Update Document

Updates an existing document in Formstack Documents.

```
PUT https://connect.mindcloud.co/v1/universal/formstackDocuments/latest/actions/update-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Formstack Documents `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/formstackDocuments/latest/actions/update-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/formstackDocuments/latest/actions/update-document', {
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
| `fileContents` | string | no | Updated base64-encoded file contents |
| `fileUrl` | string | no | Updated public file URL |
| `folder` | string | no | Updated folder name |
| `html` | string | no | Updated HTML content for HTML documents |
| `id` | string | yes | ID of the document to update |
| `name` | string | no | Updated document name |
| `output` | string | no | Updated output format |
| `outputName` | string | no | Updated merged filename |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": "string",
      "fields": [
        {}
      ],
      "id": "string",
      "key": "string",
      "name": "Ava Chen",
      "output": "string",
      "size": "string",
      "sizeHeight": "string",
      "sizeWidth": "string",
      "type": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | string |  |
| `fields` | array<object> |  |
| `id` | string |  |
| `key` | string |  |
| `name` | string |  |
| `output` | string |  |
| `size` | string |  |
| `sizeHeight` | string |  |
| `sizeWidth` | string |  |
| `type` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Formstack Documents API, this operation is `PUT /documents/:id` (base URL `https://www.webmerge.me/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-document.md) for the provider-specific parameters and requirements.

