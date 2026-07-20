# PDFMonkey: Delete Document

Deletes an existing document from PDFMonkey.

```
DELETE https://connect.mindcloud.co/v1/universal/pDFMonkey/latest/actions/delete-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PDFMonkey `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/pDFMonkey/latest/actions/delete-document?connectionId=$CONNECTION_ID&id=4ba1447a-2f06-4d47-8dc2-a1074a1aa496" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "4ba1447a-2f06-4d47-8dc2-a1074a1aa496"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pDFMonkey/latest/actions/delete-document?${params}`, {
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
| `id` | string | yes | ID of the Document to delete. Example: `4ba1447a-2f06-4d47-8dc2-a1074a1aa496`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deleted": true,
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deleted` | boolean | Whether the delete request succeeded. |
| `id` | string | Deleted document ID from the request context. |

## Native endpoint

Through the native PDFMonkey API, this operation is `DELETE /documents/:id` (base URL `https://api.pdfmonkey.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-document.md) for the provider-specific parameters and requirements.

