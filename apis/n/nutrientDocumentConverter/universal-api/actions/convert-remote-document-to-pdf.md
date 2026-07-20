# Nutrient Document Converter: Convert Remote Document to PDF

Converts a remote document to PDF in Nutrient.

```
GET https://connect.mindcloud.co/v1/universal/nutrientDocumentConverter/latest/actions/convert-remote-document-to-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nutrient Document Converter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nutrientDocumentConverter/latest/actions/convert-remote-document-to-pdf?connectionId=$CONNECTION_ID&documentUrl=https%3A%2F%2Fwww.w3.org%2FWAI%2FER%2Ftests%2Fxhtml%2Ftestfiles%2Fresources%2Fpdf%2Fdummy.pdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentUrl": "https://www.w3.org/WAI/ER/tests/xhtml/testfiles/resources/pdf/dummy.pdf"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nutrientDocumentConverter/latest/actions/convert-remote-document-to-pdf?${params}`, {
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
| `documentUrl` | string | yes | Publicly reachable source document URL. Default: `https://www.w3.org/WAI/ER/tests/xhtml/testfiles/resources/pdf/dummy.pdf`. Example: `https://www.w3.org/WAI/ER/tests/xhtml/testfiles/resources/pdf/dummy.pdf`. |

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
| `outputFile` | string | Generated PDF binary response. |

## Native endpoint

Through the native Nutrient Document Converter API, this operation is `POST /build` (base URL `https://api.nutrient.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-remote-document-to-pdf.md) for the provider-specific parameters and requirements.

