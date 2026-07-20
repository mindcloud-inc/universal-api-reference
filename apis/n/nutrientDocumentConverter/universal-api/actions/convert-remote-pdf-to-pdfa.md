# Nutrient Document Converter: Convert Remote PDF to PDF/A

Converts a remote PDF to PDF/A in Nutrient.

```
GET https://connect.mindcloud.co/v1/universal/nutrientDocumentConverter/latest/actions/convert-remote-pdf-to-pdfa
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nutrient Document Converter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nutrientDocumentConverter/latest/actions/convert-remote-pdf-to-pdfa?connectionId=$CONNECTION_ID&pdfUrl=https%3A%2F%2Fexample.com%2Fdocument.pdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pdfUrl": "https://example.com/document.pdf"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nutrientDocumentConverter/latest/actions/convert-remote-pdf-to-pdfa?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `conformance` | string | no | PDF/A conformance level, for example pdfa-2b. Default: `pdfa-2b`. |

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
| `outputFile` | string | PDF/A binary response. |

## Native endpoint

Through the native Nutrient Document Converter API, this operation is `POST /build` (base URL `https://api.nutrient.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-remote-pdf-to-pdfa.md) for the provider-specific parameters and requirements.

