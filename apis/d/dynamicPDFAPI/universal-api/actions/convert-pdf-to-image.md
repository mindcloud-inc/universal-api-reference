# DynamicPDF: Convert PDF To Image

Converts a PDF to images in DynamicPDF API.

```
GET https://connect.mindcloud.co/v1/universal/dynamicPDFAPI/latest/actions/convert-pdf-to-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DynamicPDF `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dynamicPDFAPI/latest/actions/convert-pdf-to-image?connectionId=$CONNECTION_ID&pdf=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pdf": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dynamicPDFAPI/latest/actions/convert-pdf-to-image?${params}`, {
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
| `pdf` | file | yes | The PDF document to convert to images. |
| `imageFormat` | list | no | The output image format. One of: `0`, `1`, `2`, `3`, `4`. |
| `pageCount` | number | no | How many pages to rasterize. Zero returns all pages. Example: `0`. |
| `startPageNumber` | number | no | The first page number to rasterize. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contentType": "string",
      "horizontalDpi": 1,
      "images": [
        {
          "billedPages": 1,
          "data": "string",
          "height": 1,
          "pageNumber": "string",
          "width": 1
        }
      ],
      "verticalDpi": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contentType` | string |  |
| `horizontalDpi` | number |  |
| `images[].billedPages` | number |  |
| `images[].data` | string |  |
| `images[].height` | number |  |
| `images[].pageNumber` | string |  |
| `images[].width` | number |  |
| `verticalDpi` | number |  |

## Native endpoint

Through the native DynamicPDF API, this operation is `POST /v1.0/pdf-image` (base URL `https://api.dpdf.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-pdf-to-image.md) for the provider-specific parameters and requirements.

