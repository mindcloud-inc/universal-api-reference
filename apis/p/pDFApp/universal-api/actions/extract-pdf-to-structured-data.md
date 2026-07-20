# PDF-app: Extract PDF To Structured Data

Retrieves structured data from a PDF in PDF-app.

```
GET https://connect.mindcloud.co/v1/universal/pDFApp/latest/actions/extract-pdf-to-structured-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PDF-app `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pDFApp/latest/actions/extract-pdf-to-structured-data?connectionId=$CONNECTION_ID&fileUrl=https%3A%2F%2Fwww.w3.org%2FWAI%2FER%2Ftests%2Fxhtml%2Ftestfiles%2Fresources%2Fpdf%2Fdummy.pdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileUrl": "https://www.w3.org/WAI/ER/tests/xhtml/testfiles/resources/pdf/dummy.pdf"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pDFApp/latest/actions/extract-pdf-to-structured-data?${params}`, {
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
| `fileUrl` | string | yes | PDF URL to convert and analyze. Example: `https://www.w3.org/WAI/ER/tests/xhtml/testfiles/resources/pdf/dummy.pdf`. |
| `doClassification` | boolean | no | Whether to classify entities in the extracted text. Default: `false`. |
| `doSensitivity` | boolean | no | Whether to detect PII in the extracted text. Default: `false`. |
| `onlyTables` | boolean | no | Whether to include only table data in the output file. Default: `false`. |
| `ocrPages[]` | array<number> | no | 1-based page numbers that should be forced through OCR. Example: `1,2,3`. |
| `include_pii_values` | boolean | no | Whether to return the actual PII values in detection results. Default: `false`. |
| `exclude_file_return` | boolean | no | Whether to skip generation of a downloadable output file. Default: `false`. |
| `format` | string | no | Desired output format: excel, csv, text, or none. Example: `text`. |
| `language` | string | no | OCR language code used during processing. Example: `eng`. |
| `async` | boolean | no | Whether to run the conversion asynchronously. Default: `false`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native PDF-app API returns.

## Native endpoint

Through the native PDF-app API, this operation is `POST /conv_classification` (base URL `https://api.pdf-app.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/extract-pdf-to-structured-data.md) for the provider-specific parameters and requirements.

