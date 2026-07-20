# Formstack Documents: Create Document

Creates a new document in Formstack Documents.

```
POST https://connect.mindcloud.co/v1/universal/formstackDocuments/latest/actions/create-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Formstack Documents `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/formstackDocuments/latest/actions/create-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "output": "string",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/formstackDocuments/latest/actions/create-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "output": "string",
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileContents` | string | no | Base64-encoded source file contents |
| `fileUrl` | string | no | Public URL for the source file |
| `folder` | string | no | Folder name to save the document in |
| `html` | string | no | HTML content for HTML documents |
| `name` | string | yes | Name of the document |
| `output` | string | yes | Output format to produce when merged |
| `outputName` | string | no | Custom filename for merged output |
| `type` | string | yes | Source document type |

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

Through the native Formstack Documents API, this operation is `POST /documents` (base URL `https://www.webmerge.me/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-document.md) for the provider-specific parameters and requirements.

