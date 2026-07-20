# ValidaCFDI: Validate CFDI from PDF

Validates a CFDI from a PDF in ValidaCFDI.

```
GET https://connect.mindcloud.co/v1/universal/validaCFDI/latest/actions/validate-cfdi-from-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ValidaCFDI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/validaCFDI/latest/actions/validate-cfdi-from-pdf?connectionId=$CONNECTION_ID&file=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "file": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/validaCFDI/latest/actions/validate-cfdi-from-pdf?${params}`, {
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
| `file` | file | yes | PDF invoice file to validate and extract. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "efosCheck": {},
      "errors": [
        "string"
      ],
      "extractionData": {
        "customerName": "Ava Chen",
        "extractionWarnings": [
          "string"
        ],
        "invoiceDate": "2026-05-07T12:00:00.000Z",
        "lineItems": [
          {}
        ],
        "ocrConfidence": 1,
        "rfcEmisor": "string",
        "rfcReceptor": "string",
        "supplierName": "Ava Chen",
        "total": 1,
        "uuid": "string"
      },
      "extractionSuccess": true,
      "overallStatus": "string",
      "processingTimeMs": 1,
      "timestamp": "2026-05-07T12:00:00.000Z",
      "validationPerformed": true,
      "validationResult": {},
      "verificationSuggestions": [
        "string"
      ],
      "warnings": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `efosCheck` | object | EFOS risk check result when available. |
| `errors` | array<string> | Errors returned during PDF processing. |
| `extractionData` | object | Structured data extracted from the PDF. |
| `extractionData.customerName` | string | Extracted customer name when present. |
| `extractionData.extractionWarnings` | array<string> | Warnings raised during OCR extraction. |
| `extractionData.invoiceDate` | date | Extracted invoice date when present. |
| `extractionData.lineItems` | array<object> | Extracted line items when identified. |
| `extractionData.ocrConfidence` | number | OCR confidence score for the extraction. |
| `extractionData.rfcEmisor` | string | Extracted issuer RFC when present. |
| `extractionData.rfcReceptor` | string | Extracted receiver RFC when present. |
| `extractionData.supplierName` | string | Extracted supplier name. |
| `extractionData.total` | number | Extracted invoice total when present. |
| `extractionData.uuid` | string | Extracted CFDI UUID when present. |
| `extractionSuccess` | boolean | Whether PDF extraction completed successfully. |
| `overallStatus` | string | Overall extraction and validation status. |
| `processingTimeMs` | number | Time spent processing the PDF in milliseconds. |
| `timestamp` | date | Timestamp of the PDF processing result. |
| `validationPerformed` | boolean | Whether a CFDI validation step was performed after extraction. |
| `validationResult` | object | Nested validation result when validation is performed. |
| `verificationSuggestions` | array<string> | Suggested follow-up checks when available. |
| `warnings` | array<string> | Warnings returned during PDF processing. |

## Native endpoint

Through the native ValidaCFDI API, this operation is `POST /validate/pdf` (base URL `https://api.valida-cfdi.com.mx/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-cfdi-from-pdf.md) for the provider-specific parameters and requirements.

