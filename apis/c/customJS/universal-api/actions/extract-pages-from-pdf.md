# CustomJS: Extract Pages from PDF

Extracts selected pages from a PDF in CustomJS.

```
POST https://connect.mindcloud.co/v1/universal/customJS/latest/actions/extract-pages-from-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CustomJS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/customJS/latest/actions/extract-pages-from-pdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "input.pageRange": "string",
  "input.url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/customJS/latest/actions/extract-pages-from-pdf', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "input.pageRange": "string",
    "input.url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `input.pageRange` | string | yes | Page range to extract, for example 1-3. |
| `input.url` | string | yes | URL of the PDF file to extract pages from. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        [
          1
        ]
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[]` | array<number> |  |
| `type` | string |  |

## Native endpoint

Through the native CustomJS API, this operation is `POST https://e.customjs.io/__js1-` (base URL `https://e.customjs.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/extract-pages-from-pdf.md) for the provider-specific parameters and requirements.

