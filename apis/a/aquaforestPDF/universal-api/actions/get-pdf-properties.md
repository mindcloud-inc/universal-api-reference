# Aquaforest PDF: Get PDF properties

Retrieves PDF file properties from Aquaforest PDF.

```
GET https://connect.mindcloud.co/v1/universal/aquaforestPDF/latest/actions/get-pdf-properties
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aquaforest PDF `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aquaforestPDF/latest/actions/get-pdf-properties?connectionId=$CONNECTION_ID&fileContent=JVBERi0xLjQKMSAwIG9iago8PCAvVHlwZSAvQ2F0YWxvZyAvUGFnZXMgMiAwIFIgPj4KZW5kb2JqCjIgMCBvYmoKPDwgL1R5cGUgL1BhZ2VzIC9LaWRzIFszIDAgUl0gL0NvdW50IDEgPj4KZW5kb2JqCjMgMCBvYmoKPDwgL1R5cGUgL1BhZ2UgL1BhcmVudCAyIDAgUiAvTWVkaWFCb3ggWzAgMCA2MTIgNzkyXSAvUmVzb3VyY2VzIDw8IC9Gb250IDw8IC9GMSA0IDAgUiA%2BPiA%2BPiAvQ29udGVudHMgNSAwIFIgPj4KZW5kb2JqCjQgMCBvYmoKPDwgL1R5cGUgL0ZvbnQgL1N1YnR5cGUgL1R5cGUxIC9CYXNlRm9udCAvSGVsdmV0aWNhID4%2BCmVuZG9iago1IDAgb2JqCjw8IC9MZW5ndGggMTM0ID4%2BCnN0cmVhbQpCVAovRjEgMTggVGYKNzIgNzIwIFRkCihBcXVhZm9yZXN0IHJ1bnRpbWUgdmVyaWZpY2F0aW9uKSBUagowIC0yNCBUZAooSW52b2ljZSBOdW1iZXI6IElOVi0xMjM0NSkgVGoKMCAtMjQgVGQKKFRvdGFsOiA0Mi4wMCBVU0QpIFRqCkVUCmVuZHN0cmVhbQplbmRvYmoKeHJlZgowIDYKMDAwMDAwMDAwMCA2NTUzNSBmIAowMDAwMDAwMDA5IDAwMDAwIG4gCjAwMDAwMDAwNTggMDAwMDAgbiAKMDAwMDAwMDExNSAwMDAwMCBuIAowMDAwMDAwMjQxIDAwMDAwIG4gCjAwMDAwMDAzMTEgMDAwMDAgbiAKdHJhaWxlcgo8PCAvU2l6ZSA2IC9Sb290IDEgMCBSID4%2BCnN0YXJ0eHJlZgo0OTUKJSVFT0YK" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileContent": "JVBERi0xLjQKMSAwIG9iago8PCAvVHlwZSAvQ2F0YWxvZyAvUGFnZXMgMiAwIFIgPj4KZW5kb2JqCjIgMCBvYmoKPDwgL1R5cGUgL1BhZ2VzIC9LaWRzIFszIDAgUl0gL0NvdW50IDEgPj4KZW5kb2JqCjMgMCBvYmoKPDwgL1R5cGUgL1BhZ2UgL1BhcmVudCAyIDAgUiAvTWVkaWFCb3ggWzAgMCA2MTIgNzkyXSAvUmVzb3VyY2VzIDw8IC9Gb250IDw8IC9GMSA0IDAgUiA+PiA+PiAvQ29udGVudHMgNSAwIFIgPj4KZW5kb2JqCjQgMCBvYmoKPDwgL1R5cGUgL0ZvbnQgL1N1YnR5cGUgL1R5cGUxIC9CYXNlRm9udCAvSGVsdmV0aWNhID4+CmVuZG9iago1IDAgb2JqCjw8IC9MZW5ndGggMTM0ID4+CnN0cmVhbQpCVAovRjEgMTggVGYKNzIgNzIwIFRkCihBcXVhZm9yZXN0IHJ1bnRpbWUgdmVyaWZpY2F0aW9uKSBUagowIC0yNCBUZAooSW52b2ljZSBOdW1iZXI6IElOVi0xMjM0NSkgVGoKMCAtMjQgVGQKKFRvdGFsOiA0Mi4wMCBVU0QpIFRqCkVUCmVuZHN0cmVhbQplbmRvYmoKeHJlZgowIDYKMDAwMDAwMDAwMCA2NTUzNSBmIAowMDAwMDAwMDA5IDAwMDAwIG4gCjAwMDAwMDAwNTggMDAwMDAgbiAKMDAwMDAwMDExNSAwMDAwMCBuIAowMDAwMDAwMjQxIDAwMDAwIG4gCjAwMDAwMDAzMTEgMDAwMDAgbiAKdHJhaWxlcgo8PCAvU2l6ZSA2IC9Sb290IDEgMCBSID4+CnN0YXJ0eHJlZgo0OTUKJSVFT0YK"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aquaforestPDF/latest/actions/get-pdf-properties?${params}`, {
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
| `fileContent` | file | yes | The content of the source PDF file. Default: `JVBERi0xLjQKMSAwIG9iago8PCAvVHlwZSAvQ2F0YWxvZyAvUGFnZXMgMiAwIFIgPj4KZW5kb2JqCjIgMCBvYmoKPDwgL1R5cGUgL1BhZ2VzIC9LaWRzIFszIDAgUl0gL0NvdW50IDEgPj4KZW5kb2JqCjMgMCBvYmoKPDwgL1R5cGUgL1BhZ2UgL1BhcmVudCAyIDAgUiAvTWVkaWFCb3ggWzAgMCA2MTIgNzkyXSAvUmVzb3VyY2VzIDw8IC9Gb250IDw8IC9GMSA0IDAgUiA+PiA+PiAvQ29udGVudHMgNSAwIFIgPj4KZW5kb2JqCjQgMCBvYmoKPDwgL1R5cGUgL0ZvbnQgL1N1YnR5cGUgL1R5cGUxIC9CYXNlRm9udCAvSGVsdmV0aWNhID4+CmVuZG9iago1IDAgb2JqCjw8IC9MZW5ndGggMTM0ID4+CnN0cmVhbQpCVAovRjEgMTggVGYKNzIgNzIwIFRkCihBcXVhZm9yZXN0IHJ1bnRpbWUgdmVyaWZpY2F0aW9uKSBUagowIC0yNCBUZAooSW52b2ljZSBOdW1iZXI6IElOVi0xMjM0NSkgVGoKMCAtMjQgVGQKKFRvdGFsOiA0Mi4wMCBVU0QpIFRqCkVUCmVuZHN0cmVhbQplbmRvYmoKeHJlZgowIDYKMDAwMDAwMDAwMCA2NTUzNSBmIAowMDAwMDAwMDA5IDAwMDAwIG4gCjAwMDAwMDAwNTggMDAwMDAgbiAKMDAwMDAwMDExNSAwMDAwMCBuIAowMDAwMDAwMjQxIDAwMDAwIG4gCjAwMDAwMDAzMTEgMDAwMDAgbiAKdHJhaWxlcgo8PCAvU2l6ZSA2IC9Sb290IDEgMCBSID4+CnN0YXJ0eHJlZgo0OTUKJSVFT0YK`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `pageLimit` | number | no | Maximum number of pages to process when checking hidden text or searchability. Default: `10`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "AllowAssembly": true,
      "AllowDegradedPrinting": true,
      "AllowExtractContents": true,
      "AllowExtractForAccessibility": true,
      "AllowFillInForm": true,
      "AllowModifyAnnotations": true,
      "AllowModifyContents": true,
      "AllowPrinting": true,
      "Author": "string",
      "CreationDate": "string",
      "Creator": "string",
      "ErrorMessage": "string",
      "FileSize": 1,
      "HasHiddenText": true,
      "IsEncrypted": true,
      "IsSearchable": true,
      "IsSuccessful": true,
      "Keywords": "string",
      "LicenceInfo": "string",
      "ModifiedDate": "string",
      "NumberofPages": 1,
      "PDFversion": 1,
      "Producer": "string",
      "Subject": "string",
      "Title": "string",
      "Trapped": "string",
      "XmpMetadata": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `AllowAssembly` | boolean | Whether page assembly operations are allowed. |
| `AllowDegradedPrinting` | boolean | Whether low-quality printing is allowed. |
| `AllowExtractContents` | boolean | Whether text and graphics extraction is allowed. |
| `AllowExtractForAccessibility` | boolean | Whether accessibility extraction is allowed. |
| `AllowFillInForm` | boolean | Whether filling form fields is allowed. |
| `AllowModifyAnnotations` | boolean | Whether annotation modification is allowed. |
| `AllowModifyContents` | boolean | Whether content modification is allowed. |
| `AllowPrinting` | boolean | Whether high-quality printing is allowed. |
| `Author` | string | Document author. |
| `CreationDate` | string | PDF creation date. |
| `Creator` | string | Originating application or library. |
| `ErrorMessage` | string | Error details when IsSuccessful is false. |
| `FileSize` | number | File size in bytes. |
| `HasHiddenText` | boolean | Whether the PDF has an OCR text layer. |
| `IsEncrypted` | boolean | Whether the PDF document is encrypted. |
| `IsSearchable` | boolean | Whether the PDF file is searchable. |
| `IsSuccessful` | boolean | Returns true if the action was successful. |
| `Keywords` | string | Document keywords. |
| `LicenceInfo` | string | JSON summary of the API subscription quota. |
| `ModifiedDate` | string | PDF modified date. |
| `NumberofPages` | number | The number of pages in the PDF file. |
| `PDFversion` | number | PDF specification version. |
| `Producer` | string | Product that created the PDF. |
| `Subject` | string | Document subject. |
| `Title` | string | Document title. |
| `Trapped` | string | PDF trapped metadata value. |
| `XmpMetadata` | string | XMP metadata. |

## Native endpoint

Through the native Aquaforest PDF API, this operation is `POST /GetPDFInfo` (base URL `https://aquaforest-pdf.azure-api.net/AquaforestPDFAPIV2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-pdf-properties.md) for the provider-specific parameters and requirements.

