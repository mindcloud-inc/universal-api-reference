# Nutrient Document Converter: Watermark Remote PDF

Adds a watermark to a remote PDF in Nutrient.

```
GET https://connect.mindcloud.co/v1/universal/nutrientDocumentConverter/latest/actions/watermark-remote-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nutrient Document Converter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nutrientDocumentConverter/latest/actions/watermark-remote-pdf?connectionId=$CONNECTION_ID&pdfUrl=https%3A%2F%2Fexample.com%2Fdocument.pdf&text=CONFIDENTIAL" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pdfUrl": "https://example.com/document.pdf",
  "text": "CONFIDENTIAL"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nutrientDocumentConverter/latest/actions/watermark-remote-pdf?${params}`, {
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
| `pdfUrl` | string | yes | Publicly reachable PDF URL. Example: `https://example.com/document.pdf`. |
| `text` | string | yes | Text to add as a watermark. Default: `CONFIDENTIAL`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `opacity` | number | no | Watermark opacity from 0 to 1. Default: `0.5`. |

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
| `outputFile` | string | Watermarked PDF binary response. |

## Native endpoint

Through the native Nutrient Document Converter API, this operation is `POST /build` (base URL `https://api.nutrient.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/watermark-remote-pdf.md) for the provider-specific parameters and requirements.

