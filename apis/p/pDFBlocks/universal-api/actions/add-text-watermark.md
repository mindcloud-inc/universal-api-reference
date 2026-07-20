# PDF Blocks: Add Text Watermark

Updates a PDF document with a text watermark in PDF Blocks.

```
PUT https://connect.mindcloud.co/v1/universal/pDFBlocks/latest/actions/add-text-watermark
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PDF Blocks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pDFBlocks/latest/actions/add-text-watermark" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string",
  "line1": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pDFBlocks/latest/actions/add-text-watermark', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string",
    "line1": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | file | yes | The input PDF document. |
| `line1` | string | yes | The first line of text of the watermark. |
| `line2` | string | no | The second line of text of the watermark. |
| `line3` | string | no | The third line of text of the watermark. |
| `template` | number | no | The text watermark template ID. |
| `color` | string | no | The color of the text watermark. |
| `transparency` | number | no | The transparency level for the text watermark. |
| `margin` | number | no | The distance in inches from the border of the page to the text watermark. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native PDF Blocks API returns.

## Native endpoint

Through the native PDF Blocks API, this operation is `POST /v1/add_watermark/text` (base URL `https://api.pdfblocks.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-text-watermark.md) for the provider-specific parameters and requirements.

