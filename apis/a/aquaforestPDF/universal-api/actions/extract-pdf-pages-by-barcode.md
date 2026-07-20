# Aquaforest PDF: Extract PDF pages by barcode

Extracts PDF pages by barcode matches in Aquaforest PDF.

```
POST https://connect.mindcloud.co/v1/universal/aquaforestPDF/latest/actions/extract-pdf-pages-by-barcode
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aquaforest PDF `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/aquaforestPDF/latest/actions/extract-pdf-pages-by-barcode" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fileContent": "JVBERi0xLjQKMSAwIG9iago8PCAvVHlwZSAvQ2F0YWxvZyAvUGFnZXMgMiAwIFIgPj4KZW5kb2JqCjIgMCBvYmoKPDwgL1R5cGUgL1BhZ2VzIC9LaWRzIFszIDAgUl0gL0NvdW50IDEgPj4KZW5kb2JqCjMgMCBvYmoKPDwgL1R5cGUgL1BhZ2UgL1BhcmVudCAyIDAgUiAvTWVkaWFCb3ggWzAgMCA2MTIgNzkyXSAvUmVzb3VyY2VzIDw8IC9Gb250IDw8IC9GMSA0IDAgUiA+PiA+PiAvQ29udGVudHMgNSAwIFIgPj4KZW5kb2JqCjQgMCBvYmoKPDwgL1R5cGUgL0ZvbnQgL1N1YnR5cGUgL1R5cGUxIC9CYXNlRm9udCAvSGVsdmV0aWNhID4+CmVuZG9iago1IDAgb2JqCjw8IC9MZW5ndGggMTM0ID4+CnN0cmVhbQpCVAovRjEgMTggVGYKNzIgNzIwIFRkCihBcXVhZm9yZXN0IHJ1bnRpbWUgdmVyaWZpY2F0aW9uKSBUagowIC0yNCBUZAooSW52b2ljZSBOdW1iZXI6IElOVi0xMjM0NSkgVGoKMCAtMjQgVGQKKFRvdGFsOiA0Mi4wMCBVU0QpIFRqCkVUCmVuZHN0cmVhbQplbmRvYmoKeHJlZgowIDYKMDAwMDAwMDAwMCA2NTUzNSBmIAowMDAwMDAwMDA5IDAwMDAwIG4gCjAwMDAwMDAwNTggMDAwMDAgbiAKMDAwMDAwMDExNSAwMDAwMCBuIAowMDAwMDAwMjQxIDAwMDAwIG4gCjAwMDAwMDAzMTEgMDAwMDAgbiAKdHJhaWxlcgo8PCAvU2l6ZSA2IC9Sb290IDEgMCBSID4+CnN0YXJ0eHJlZgo0OTUKJSVFT0YK",
  "sourceFileName": "aquaforest-runtime.pdf",
  "fileNameTemplate": "%VALUE1%.pdf",
  "noTextFileName": "NoBarcode_%FILENAME%"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aquaforestPDF/latest/actions/extract-pdf-pages-by-barcode', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fileContent": "JVBERi0xLjQKMSAwIG9iago8PCAvVHlwZSAvQ2F0YWxvZyAvUGFnZXMgMiAwIFIgPj4KZW5kb2JqCjIgMCBvYmoKPDwgL1R5cGUgL1BhZ2VzIC9LaWRzIFszIDAgUl0gL0NvdW50IDEgPj4KZW5kb2JqCjMgMCBvYmoKPDwgL1R5cGUgL1BhZ2UgL1BhcmVudCAyIDAgUiAvTWVkaWFCb3ggWzAgMCA2MTIgNzkyXSAvUmVzb3VyY2VzIDw8IC9Gb250IDw8IC9GMSA0IDAgUiA+PiA+PiAvQ29udGVudHMgNSAwIFIgPj4KZW5kb2JqCjQgMCBvYmoKPDwgL1R5cGUgL0ZvbnQgL1N1YnR5cGUgL1R5cGUxIC9CYXNlRm9udCAvSGVsdmV0aWNhID4+CmVuZG9iago1IDAgb2JqCjw8IC9MZW5ndGggMTM0ID4+CnN0cmVhbQpCVAovRjEgMTggVGYKNzIgNzIwIFRkCihBcXVhZm9yZXN0IHJ1bnRpbWUgdmVyaWZpY2F0aW9uKSBUagowIC0yNCBUZAooSW52b2ljZSBOdW1iZXI6IElOVi0xMjM0NSkgVGoKMCAtMjQgVGQKKFRvdGFsOiA0Mi4wMCBVU0QpIFRqCkVUCmVuZHN0cmVhbQplbmRvYmoKeHJlZgowIDYKMDAwMDAwMDAwMCA2NTUzNSBmIAowMDAwMDAwMDA5IDAwMDAwIG4gCjAwMDAwMDAwNTggMDAwMDAgbiAKMDAwMDAwMDExNSAwMDAwMCBuIAowMDAwMDAwMjQxIDAwMDAwIG4gCjAwMDAwMDAzMTEgMDAwMDAgbiAKdHJhaWxlcgo8PCAvU2l6ZSA2IC9Sb290IDEgMCBSID4+CnN0YXJ0eHJlZgo0OTUKJSVFT0YK",
    "sourceFileName": "aquaforest-runtime.pdf",
    "fileNameTemplate": "%VALUE1%.pdf",
    "noTextFileName": "NoBarcode_%FILENAME%"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileContent` | file | yes | The content of the source PDF file. Default: `JVBERi0xLjQKMSAwIG9iago8PCAvVHlwZSAvQ2F0YWxvZyAvUGFnZXMgMiAwIFIgPj4KZW5kb2JqCjIgMCBvYmoKPDwgL1R5cGUgL1BhZ2VzIC9LaWRzIFszIDAgUl0gL0NvdW50IDEgPj4KZW5kb2JqCjMgMCBvYmoKPDwgL1R5cGUgL1BhZ2UgL1BhcmVudCAyIDAgUiAvTWVkaWFCb3ggWzAgMCA2MTIgNzkyXSAvUmVzb3VyY2VzIDw8IC9Gb250IDw8IC9GMSA0IDAgUiA+PiA+PiAvQ29udGVudHMgNSAwIFIgPj4KZW5kb2JqCjQgMCBvYmoKPDwgL1R5cGUgL0ZvbnQgL1N1YnR5cGUgL1R5cGUxIC9CYXNlRm9udCAvSGVsdmV0aWNhID4+CmVuZG9iago1IDAgb2JqCjw8IC9MZW5ndGggMTM0ID4+CnN0cmVhbQpCVAovRjEgMTggVGYKNzIgNzIwIFRkCihBcXVhZm9yZXN0IHJ1bnRpbWUgdmVyaWZpY2F0aW9uKSBUagowIC0yNCBUZAooSW52b2ljZSBOdW1iZXI6IElOVi0xMjM0NSkgVGoKMCAtMjQgVGQKKFRvdGFsOiA0Mi4wMCBVU0QpIFRqCkVUCmVuZHN0cmVhbQplbmRvYmoKeHJlZgowIDYKMDAwMDAwMDAwMCA2NTUzNSBmIAowMDAwMDAwMDA5IDAwMDAwIG4gCjAwMDAwMDAwNTggMDAwMDAgbiAKMDAwMDAwMDExNSAwMDAwMCBuIAowMDAwMDAwMjQxIDAwMDAwIG4gCjAwMDAwMDAzMTEgMDAwMDAgbiAKdHJhaWxlcgo8PCAvU2l6ZSA2IC9Sb290IDEgMCBSID4+CnN0YXJ0eHJlZgo0OTUKJSVFT0YK`. |
| `sourceFileName` | string | yes | The name of the source file. Default: `aquaforest-runtime.pdf`. |
| `fileNameTemplate` | string | yes | Template for the output file if barcode is found. Default: `%VALUE1%.pdf`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `noTextFileName` | string | yes | Template for the output file if no barcode is found. Default: `NoBarcode_%FILENAME%`. |
| `zones[]` | array<object> | no | Barcode extraction zone objects with location, barcodeFormats, and optional regex. Default: `[{"location":"all","barcodeFormats":["All 1D"]}]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ErrorMessage": "string",
      "IsSuccessful": true,
      "LicenceInfo": "string",
      "SplittedFile": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ErrorMessage` | string | Error details when IsSuccessful is false. |
| `IsSuccessful` | boolean | Whether at least one page was extracted. |
| `LicenceInfo` | string | API subscription key information. |
| `SplittedFile` | array<object> | Extracted output files with file content, generated file name, and page number. |

## Native endpoint

Through the native Aquaforest PDF API, this operation is `POST /ExtractPageByBarcode` (base URL `https://aquaforest-pdf.azure-api.net/AquaforestPDFAPIV2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/extract-pdf-pages-by-barcode.md) for the provider-specific parameters and requirements.

