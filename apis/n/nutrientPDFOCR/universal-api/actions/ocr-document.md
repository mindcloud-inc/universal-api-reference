# Nutrient - PDF OCR: OCR Document

Retrieves a searchable PDF from Nutrient using OCR.

```
GET https://connect.mindcloud.co/v1/universal/nutrientPDFOCR/latest/actions/ocr-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nutrient - PDF OCR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nutrientPDFOCR/latest/actions/ocr-document?connectionId=$CONNECTION_ID&file=Upload%20a%20scanned%20PDF%20or%20image%20file&data.language=english" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "file": "Upload a scanned PDF or image file",
  "data.language": "english"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nutrientPDFOCR/latest/actions/ocr-document?${params}`, {
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
| `file` | file | yes | Image or scanned document to run OCR on. Example: `Upload a scanned PDF or image file`. |
| `data.language` | string | yes | OCR language to use. Nutrient's example uses english. Default: `english`. Example: `english`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pdf": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pdf` | string | Base64-encoded searchable PDF returned by the OCR endpoint when captured as a raw response. |

## Native endpoint

Through the native Nutrient - PDF OCR API, this operation is `POST /processor/ocr` (base URL `https://api.nutrient.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/ocr-document.md) for the provider-specific parameters and requirements.

