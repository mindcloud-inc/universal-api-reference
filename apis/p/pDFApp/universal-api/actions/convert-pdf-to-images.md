# PDF-app: Convert PDF To Images

Creates image files from a PDF in PDF-app.

```
POST https://connect.mindcloud.co/v1/universal/pDFApp/latest/actions/convert-pdf-to-images
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PDF-app `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pDFApp/latest/actions/convert-pdf-to-images" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "pdfUrls[]": [
    "https://example.com"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pDFApp/latest/actions/convert-pdf-to-images', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "pdfUrls[]": ["https://example.com"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `pdfUrls[]` | array<string> | yes | Public URLs of the PDF files to convert into images. |
| `imageType` | string | no | Output image format for the converted pages, such as jpeg or png. |
| `async` | boolean | no | Run the conversion asynchronously and fetch the result later by job ID. |
| `fileName` | string | no | Optional base filename for the generated image files. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `quality` | number | no | Output image quality from 72 to 400. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native PDF-app API returns.

## Native endpoint

Through the native PDF-app API, this operation is `POST /pdf_to_image` (base URL `https://api.pdf-app.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-pdf-to-images.md) for the provider-specific parameters and requirements.

