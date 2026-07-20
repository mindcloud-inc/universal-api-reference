# Veryfi OCR: Unlink Tag From Document

Unlinks a tag from a document in Veryfi OCR.

```
DELETE https://connect.mindcloud.co/v1/universal/veryfiOCR/latest/actions/unlink-tag-from-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Veryfi OCR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/veryfiOCR/latest/actions/unlink-tag-from-document?connectionId=$CONNECTION_ID&documentId=string&tagId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentId": "string",
  "tagId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/veryfiOCR/latest/actions/unlink-tag-from-document?${params}`, {
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
| `documentId` | string | yes | The Veryfi document identifier. |
| `tagId` | string | yes | The Veryfi tag identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Veryfi OCR API, this operation is `DELETE /api/v8/partner/documents/:document_id/tags/:tag_id` (base URL `https://api.veryfi.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/unlink-tag-from-document.md) for the provider-specific parameters and requirements.

