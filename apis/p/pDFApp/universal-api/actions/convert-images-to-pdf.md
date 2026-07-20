# PDF-app: Convert Images To PDF

Creates a PDF from image files in PDF-app.

```
POST https://connect.mindcloud.co/v1/universal/pDFApp/latest/actions/convert-images-to-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PDF-app `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pDFApp/latest/actions/convert-images-to-pdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "imageUrls[]": [
    "https://example.com"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pDFApp/latest/actions/convert-images-to-pdf', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "imageUrls[]": ["https://example.com"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `imageUrls[]` | array<string> | yes | Public image URLs to combine into a PDF in order. |
| `async` | boolean | no | Set true to queue the conversion asynchronously. |
| `fileName` | string | no | Optional output file name for the created PDF. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native PDF-app API returns.

## Native endpoint

Through the native PDF-app API, this operation is `POST /image_to_pdf` (base URL `https://api.pdf-app.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-images-to-pdf.md) for the provider-specific parameters and requirements.

