# Nutrient Document Converter: Protect Remote PDF

Protects a remote PDF in Nutrient.

```
GET https://connect.mindcloud.co/v1/universal/nutrientDocumentConverter/latest/actions/protect-remote-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nutrient Document Converter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nutrientDocumentConverter/latest/actions/protect-remote-pdf?connectionId=$CONNECTION_ID&pdfUrl=https%3A%2F%2Fexample.com%2Fdocument.pdf&userPassword=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pdfUrl": "https://example.com/document.pdf",
  "userPassword": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nutrientDocumentConverter/latest/actions/protect-remote-pdf?${params}`, {
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
| `userPassword` | string | yes | Password required to open the output PDF. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ownerPassword` | string | no | Owner password used to control permissions. |
| `allowPrinting` | boolean | no | Whether printing is allowed in the output PDF. Default: `false`. |

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
| `outputFile` | string | Protected PDF binary response. |

## Native endpoint

Through the native Nutrient Document Converter API, this operation is `POST /build` (base URL `https://api.nutrient.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/protect-remote-pdf.md) for the provider-specific parameters and requirements.

