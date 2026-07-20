# PDF-app: Run OCR

Retrieves OCR text from a file in PDF-app.

```
GET https://connect.mindcloud.co/v1/universal/pDFApp/latest/actions/run-ocr
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PDF-app `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pDFApp/latest/actions/run-ocr?connectionId=$CONNECTION_ID&fileUrls%5B%5D=https%3A%2F%2Fwww.w3.org%2FWAI%2FER%2Ftests%2Fxhtml%2Ftestfiles%2Fresources%2Fpdf%2Fdummy.pdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileUrls[]": "https://www.w3.org/WAI/ER/tests/xhtml/testfiles/resources/pdf/dummy.pdf"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pDFApp/latest/actions/run-ocr?${params}`, {
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
| `versionMode` | string | no | OCR engine version mode; use 2 for the Textract-based V2 flow. Example: `2`. |
| `fileUrls[]` | array<string> | yes | Document URLs to run through OCR. Example: `https://www.w3.org/WAI/ER/tests/xhtml/testfiles/resources/pdf/dummy.pdf`. |
| `v2rawText` | boolean | no | Whether to extract raw text lines in OCR V2. Default: `true`. |
| `v2Layout` | boolean | no | Whether to include layout blocks and bounding boxes. Default: `false`. |
| `v2Forms` | boolean | no | Whether to extract key-value form pairs. Default: `false`. |
| `v2Tables` | boolean | no | Whether to extract tables from the document. Default: `false`. |
| `v2Signatures` | boolean | no | Whether to detect signatures in the document. Default: `false`. |
| `async` | boolean | no | Whether to run OCR asynchronously. Default: `false`. |
| `pdfConvertZoomFactor` | number | no | Zoom factor used when converting PDFs before OCR. Example: `1`. |
| `zoom_factor_img` | number | no | Scaling factor applied to images before OCR. Example: `1`. |
| `regions[]` | array<object> | no | Optional region definitions for targeted OCR extraction. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creditsConsumed": 1,
      "creditsRemaining": 1,
      "extraction_results": [
        {}
      ],
      "job_id": "string",
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creditsConsumed` | number | Credits consumed by the OCR request. |
| `creditsRemaining` | number | Remaining provider credits after the OCR request. |
| `extraction_results` | array<object> | OCR extraction results grouped by file and page. |
| `job_id` | string | Provider job identifier for the OCR request. |
| `message` | string | Summary of the OCR completion status. |

## Native endpoint

Through the native PDF-app API, this operation is `POST /ocr` (base URL `https://api.pdf-app.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/run-ocr.md) for the provider-specific parameters and requirements.

