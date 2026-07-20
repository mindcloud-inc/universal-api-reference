# Feishu Document: Create Document

Creates a new document in Feishu Docs.

```
POST https://connect.mindcloud.co/v1/universal/feishuDocument/latest/actions/create-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Feishu Document `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/feishuDocument/latest/actions/create-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/feishuDocument/latest/actions/create-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | no | Optional document title. Lark limits the title to 1-800 characters when provided. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "data": {
        "document": {
          "document_id": "string",
          "revision_id": 1,
          "title": "string"
        }
      },
      "msg": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number | Provider error code. Zero means success. |
| `data.document.document_id` | string | Created document token returned by Feishu. |
| `data.document.revision_id` | number | Initial document revision id. |
| `data.document.title` | string | Document title returned by Feishu. |
| `msg` | string | Provider status message. |

## Native endpoint

Through the native Feishu Document API, this operation is `POST /open-apis/docx/v1/documents` (base URL `https://open.larksuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-document.md) for the provider-specific parameters and requirements.

