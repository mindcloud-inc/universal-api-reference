# PDF Blocks: Rotate Pages

Updates a PDF document by rotating pages in PDF Blocks.

```
PUT https://connect.mindcloud.co/v1/universal/pDFBlocks/latest/actions/rotate-pages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PDF Blocks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pDFBlocks/latest/actions/rotate-pages" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string",
  "angle": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pDFBlocks/latest/actions/rotate-pages', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string",
    "angle": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | file | yes | The input PDF document. |
| `angle` | number | yes | The angle of rotation of the pages. |
| `firstPage` | number | no | The first page of the range to rotate in the PDF document. |
| `lastPage` | number | no | The last page of the range to rotate in the PDF document. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native PDF Blocks API returns.

## Native endpoint

Through the native PDF Blocks API, this operation is `POST /v1/rotate_pages` (base URL `https://api.pdfblocks.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/rotate-pages.md) for the provider-specific parameters and requirements.

