# Cloudmersive Document Conversion: Convert HTML String to PDF

Converts an HTML string to PDF.

```
GET https://connect.mindcloud.co/v1/universal/cloudmersiveDocumentConversion/latest/actions/convert-html-string-to-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudmersive Document Conversion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudmersiveDocumentConversion/latest/actions/convert-html-string-to-pdf?connectionId=$CONNECTION_ID&html=%3Ch1%3ECloudmersive%20Document%20Conversion%3C%2Fh1%3E" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "html": "<h1>Cloudmersive Document Conversion</h1>"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudmersiveDocumentConversion/latest/actions/convert-html-string-to-pdf?${params}`, {
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
| `html` | string | yes | HTML string to render into a PDF. Default: `<h1>Cloudmersive Document Conversion</h1>`. |
| `extraLoadingWait` | number | no | Optional extra wait time in milliseconds for dynamic content. Maximum is 30000. Default: `0`. |
| `includeBackgroundGraphics` | boolean | no | Optional. Set true to include background graphics in the PDF; default is true. Default: `true`. |
| `scaleFactor` | number | no | Optional scale factor percentage. Default is 100. Default: `100`. |
| `autoSanitize` | boolean | no | Optional. Automatically sanitize unsafe HTML elements. Default is true. Default: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "outputFile": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `outputFile` | string | Converted PDF file content returned by Cloudmersive. |

## Native endpoint

Through the native Cloudmersive Document Conversion API, this operation is `POST /convert/web/html/to/pdf` (base URL `https://api.cloudmersive.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-html-string-to-pdf.md) for the provider-specific parameters and requirements.

