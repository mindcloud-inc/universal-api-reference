# KiteSuite: List Workspace Documents

Retrieves workspace documents from KiteSuite.

```
GET https://connect.mindcloud.co/v1/universal/kiteSuite/latest/actions/list-workspace-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KiteSuite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kiteSuite/latest/actions/list-workspace-documents?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kiteSuite/latest/actions/list-workspace-documents?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "childNodes": [
        "string"
      ],
      "documentName": "Ava Chen",
      "file": {},
      "isTrashed": true,
      "owner": "string",
      "pages": [
        "string"
      ],
      "parentNodes": [
        "string"
      ],
      "project": "string",
      "type": "string",
      "workspace": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string | Document ID. |
| `childNodes` | array<string> | Child document or page IDs. |
| `documentName` | string | Document title. |
| `file` | object | File metadata for the document. |
| `isTrashed` | boolean | Whether the document is trashed. |
| `owner` | string | Owner of the document. |
| `pages` | array<string> | Document page IDs. |
| `parentNodes` | array<string> | Parent document IDs. |
| `project` | string | Project ID of the document. |
| `type` | string | Document type. |
| `workspace` | string | Workspace ID of the document. |

## Native endpoint

Through the native KiteSuite API, this operation is `GET /api/v1/document` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-workspace-documents.md) for the provider-specific parameters and requirements.

