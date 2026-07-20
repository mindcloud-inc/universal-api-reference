# Cloudmersive Document Conversion: Convert URL to PDF

Converts a website URL to PDF.

```
GET https://connect.mindcloud.co/v1/universal/cloudmersiveDocumentConversion/latest/actions/convert-url-to-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudmersive Document Conversion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudmersiveDocumentConversion/latest/actions/convert-url-to-pdf?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudmersiveDocumentConversion/latest/actions/convert-url-to-pdf?${params}`, {
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
| `url` | string | yes | Website URL to render into a PDF. Default: `https://example.com`. |
| `extraLoadingWait` | number | no | Optional extra wait time in milliseconds for page rendering. Maximum is 20000. Default: `0`. |
| `includeBackgroundGraphics` | boolean | no | Optional. Set true to include background graphics in the PDF; default is true. Default: `true`. |
| `scaleFactor` | number | no | Optional scale factor percentage. Default is 100. Default: `100`. |

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

Through the native Cloudmersive Document Conversion API, this operation is `POST /convert/web/url/to/pdf` (base URL `https://api.cloudmersive.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-url-to-pdf.md) for the provider-specific parameters and requirements.

