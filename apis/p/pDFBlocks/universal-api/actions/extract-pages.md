# PDF Blocks: Extract Pages

Creates a PDF document with extracted pages in PDF Blocks.

```
POST https://connect.mindcloud.co/v1/universal/pDFBlocks/latest/actions/extract-pages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PDF Blocks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pDFBlocks/latest/actions/extract-pages" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pDFBlocks/latest/actions/extract-pages', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | file | yes | The input PDF document. |
| `firstPage` | number | no | The first page of the range to extract. |
| `lastPage` | number | no | The last page of the range to extract. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native PDF Blocks API returns.

## Native endpoint

Through the native PDF Blocks API, this operation is `POST /v1/extract_pages` (base URL `https://api.pdfblocks.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/extract-pages.md) for the provider-specific parameters and requirements.

