# Conveyor: Update Document

Updates a document in the Conveyor exchange.

```
PUT https://connect.mindcloud.co/v1/universal/conveyor/latest/actions/update-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Conveyor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/conveyor/latest/actions/update-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "documentId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/conveyor/latest/actions/update-document', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "documentId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `documentId` | string | yes | Document identifier. |
| `name` | string | no | Document name. |
| `file` | file | no | Replacement document file upload. |
| `description` | string | no | Document description. |
| `certification` | string | no | Document certification type. |
| `featured` | boolean | no | Whether the document is featured. |
| `folderId` | string | no | Folder identifier to place the document in. |
| `accessLevel` | string | no | Document access level. |
| `productLineIds` | string<string> | no | Product line identifiers for the document. |
| `accessGroupIds` | string<string> | no | Access group identifiers for the document. |
| `disableDownloads` | boolean | no | Whether downloads are disabled. |
| `useForQuestionAnswering` | boolean | no | Whether to use the document for question answering. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "access_groups": [
        {
          "id": "string",
          "name": "Ava Chen"
        }
      ],
      "access_level": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "display_certification": "string",
      "featured": true,
      "file_updated_at": "2026-05-07T12:00:00.000Z",
      "folder": "string",
      "id": "string",
      "name": "Ava Chen",
      "product_lines": [
        {
          "id": "string",
          "name": "Ava Chen"
        }
      ],
      "publicly_accessible": true,
      "updated_at": "2026-05-07T12:00:00.000Z",
      "versions": [
        {
          "id": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `access_groups` | array<object> |  |
| `access_groups[].id` | string |  |
| `access_groups[].name` | string |  |
| `access_level` | string |  |
| `created_at` | date |  |
| `description` | string |  |
| `display_certification` | string |  |
| `featured` | boolean |  |
| `file_updated_at` | date |  |
| `folder` | string |  |
| `id` | string |  |
| `name` | string |  |
| `product_lines` | array<object> |  |
| `product_lines[].id` | string |  |
| `product_lines[].name` | string |  |
| `publicly_accessible` | boolean |  |
| `updated_at` | date |  |
| `versions` | array<object> |  |
| `versions[].id` | string |  |

## Native endpoint

Through the native Conveyor API, this operation is `PATCH /v2/exchange/documents/:document_id` (base URL `https://api.conveyor.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-document.md) for the provider-specific parameters and requirements.

