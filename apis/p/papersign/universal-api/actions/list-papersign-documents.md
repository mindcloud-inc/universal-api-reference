# Papersign: List Papersign Documents



```
GET https://connect.mindcloud.co/v1/universal/papersign/latest/actions/list-papersign-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Papersign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/papersign/latest/actions/list-papersign-documents?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/papersign/latest/actions/list-papersign-documents?${params}`, {
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
      "has_more": true,
      "limit": 1,
      "results": {
        "documents": [
          {
            "completed_at_utc": "2026-05-07T12:00:00.000Z",
            "created_at_utc": "2026-05-07T12:00:00.000Z",
            "folder": {
              "id": 1,
              "name": "Ava Chen",
              "space_id": 1
            },
            "id": "string",
            "name": "Ava Chen",
            "sent_at_utc": "2026-05-07T12:00:00.000Z",
            "space": {
              "id": 1,
              "name": "Ava Chen"
            },
            "status": "string",
            "updated_at_utc": "2026-05-07T12:00:00.000Z"
          }
        ]
      },
      "skip": 1,
      "status": "string",
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `has_more` | boolean | Whether more documents are available. |
| `limit` | number | The page size used for the response. |
| `results.documents[].completed_at_utc` | date | The time the document was completed. |
| `results.documents[].created_at_utc` | date | The time the document was created. |
| `results.documents[].folder.id` | number | The unique identifier of the folder. |
| `results.documents[].folder.name` | string | The name of the folder. |
| `results.documents[].folder.space_id` | number | The unique identifier of the space that owns the folder. |
| `results.documents[].id` | string | The unique identifier of the document. |
| `results.documents[].name` | string | The name of the document. |
| `results.documents[].sent_at_utc` | date | The time the document was sent. |
| `results.documents[].space.id` | number | The unique identifier of the space. |
| `results.documents[].space.name` | string | The name of the space. |
| `results.documents[].status` | string | The status of the document. |
| `results.documents[].updated_at_utc` | date | The time the document was last updated. |
| `skip` | number | The number of skipped records. |
| `status` | string | Response status. |
| `total` | number | The total number of documents. |

## Native endpoint

Through the native Papersign API, this operation is `GET /papersign/documents` (base URL `https://api.paperform.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-papersign-documents.md) for the provider-specific parameters and requirements.

