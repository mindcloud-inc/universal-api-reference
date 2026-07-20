# Koncile OCR: Delete Document



```
DELETE https://connect.mindcloud.co/v1/universal/koncileOCR/latest/actions/delete-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Koncile OCR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/koncileOCR/latest/actions/delete-document?connectionId=$CONNECTION_ID&doc_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "doc_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/koncileOCR/latest/actions/delete-document?${params}`, {
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
| `delete_file` | boolean | no | Also delete the underlying stored file when true. |
| `doc_id` | number | yes | Delete this document ID from Koncile. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "doc_id": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `doc_id` | number | The deleted document identifier. |
| `success` | boolean | Whether the delete request succeeded. |

## Native endpoint

Through the native Koncile OCR API, this operation is `DELETE /delete_doc` (base URL `https://api.koncile.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-document.md) for the provider-specific parameters and requirements.

