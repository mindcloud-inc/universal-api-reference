# Nutrient Document Converter: Convert Remote Document to Image

Converts a remote document to images in Nutrient.

```
GET https://connect.mindcloud.co/v1/universal/nutrientDocumentConverter/latest/actions/convert-remote-document-to-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nutrient Document Converter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nutrientDocumentConverter/latest/actions/convert-remote-document-to-image?connectionId=$CONNECTION_ID&documentUrl=https%3A%2F%2Fexample.com%2Fdocument.docx" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentUrl": "https://example.com/document.docx"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nutrientDocumentConverter/latest/actions/convert-remote-document-to-image?${params}`, {
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
| `documentUrl` | string | yes | Publicly reachable source document URL. Example: `https://example.com/document.docx`. |
| `format` | string | no | Image format to output. Default: `jpg`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `width` | number | no | Optional output width in pixels. Default: `768`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contentType": "string",
      "outputFile": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contentType` | string | Response content type. |
| `outputFile` | string | Generated image or ZIP binary response. |

## Native endpoint

Through the native Nutrient Document Converter API, this operation is `POST /build` (base URL `https://api.nutrient.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-remote-document-to-image.md) for the provider-specific parameters and requirements.

