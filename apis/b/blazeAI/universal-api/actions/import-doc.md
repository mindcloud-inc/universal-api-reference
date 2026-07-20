# Blaze AI: Import Doc

Creates a document import in Blaze AI.

```
POST https://connect.mindcloud.co/v1/universal/blazeAI/latest/actions/import-doc
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Blaze AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/blazeAI/latest/actions/import-doc" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspace_id": "994619",
  "importFile": "https://calibre-ebook.com/downloads/demos/demo.docx",
  "importSource": "docx"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/blazeAI/latest/actions/import-doc', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspace_id": "994619",
    "importFile": "https://calibre-ebook.com/downloads/demos/demo.docx",
    "importSource": "docx"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspace_id` | number | yes | Default: `994619`. |
| `importFile` | string | yes | Default: `https://calibre-ebook.com/downloads/demos/demo.docx`. |
| `importSource` | string | yes | Default: `docx`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "doc": {
          "id": 1,
          "key": "string",
          "title": "string"
        },
        "id": 1,
        "status": "string"
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.doc.id` | number |  |
| `data.doc.key` | string |  |
| `data.doc.title` | string |  |
| `data.id` | number |  |
| `data.status` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Blaze AI API, this operation is `POST /api/v1/w/:workspace_id/imports` (base URL `https://api.blaze.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/import-doc.md) for the provider-specific parameters and requirements.

