# Rossum: Retrieve Document

Retrieves a document from Rossum.

```
GET https://connect.mindcloud.co/v1/universal/rossum/latest/actions/retrieve-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rossum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rossum/latest/actions/retrieve-document?connectionId=$CONNECTION_ID&documentID=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentID": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rossum/latest/actions/retrieve-document?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `documentID` | number | yes | ID of the document to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "annotations": [
        "string"
      ],
      "attachment_status": "string",
      "content": "string",
      "email": "ava@example.com",
      "id": 1,
      "mime_type": "string",
      "original_file_name": "Ava Chen",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `annotations` | array<string> | Related annotation URLs. |
| `attachment_status` | string | Processing status. |
| `content` | string | Document content URL. |
| `email` | string | Related email URL. |
| `id` | number | Rossum document ID. |
| `mime_type` | string | Document MIME type. |
| `original_file_name` | string | Original uploaded filename. |
| `url` | string | Document URL. |

## Native endpoint

Through the native Rossum API, this operation is `GET /documents/:documentID` (base URL `https://mindcloud.rossum.app/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-document.md) for the provider-specific parameters and requirements.

