# Aquaforest PDF: Get data from PDF

Retrieves key-value data from PDFs in Aquaforest PDF.

```
GET https://connect.mindcloud.co/v1/universal/aquaforestPDF/latest/actions/get-data-from-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aquaforest PDF `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aquaforestPDF/latest/actions/get-data-from-pdf?connectionId=$CONNECTION_ID&fileContent=JVBERi0xLjQKMSAwIG9iago8PCAvVHlwZSAvQ2F0YWxvZyAvUGFnZXMgMiAwIFIgPj4KZW5kb2JqCjIgMCBvYmoKPDwgL1R5cGUgL1BhZ2VzIC9LaWRzIFszIDAgUl0gL0NvdW50IDEgPj4KZW5kb2JqCjMgMCBvYmoKPDwgL1R5cGUgL1BhZ2UgL1BhcmVudCAyIDAgUiAvTWVkaWFCb3ggWzAgMCA2MTIgNzkyXSAvUmVzb3VyY2VzIDw8IC9Gb250IDw8IC9GMSA0IDAgUiA%2BPiA%2BPiAvQ29udGVudHMgNSAwIFIgPj4KZW5kb2JqCjQgMCBvYmoKPDwgL1R5cGUgL0ZvbnQgL1N1YnR5cGUgL1R5cGUxIC9CYXNlRm9udCAvSGVsdmV0aWNhID4%2BCmVuZG9iago1IDAgb2JqCjw8IC9MZW5ndGggMTM0ID4%2BCnN0cmVhbQpCVAovRjEgMTggVGYKNzIgNzIwIFRkCihBcXVhZm9yZXN0IHJ1bnRpbWUgdmVyaWZpY2F0aW9uKSBUagowIC0yNCBUZAooSW52b2ljZSBOdW1iZXI6IElOVi0xMjM0NSkgVGoKMCAtMjQgVGQKKFRvdGFsOiA0Mi4wMCBVU0QpIFRqCkVUCmVuZHN0cmVhbQplbmRvYmoKeHJlZgowIDYKMDAwMDAwMDAwMCA2NTUzNSBmIAowMDAwMDAwMDA5IDAwMDAwIG4gCjAwMDAwMDAwNTggMDAwMDAgbiAKMDAwMDAwMDExNSAwMDAwMCBuIAowMDAwMDAwMjQxIDAwMDAwIG4gCjAwMDAwMDAzMTEgMDAwMDAgbiAKdHJhaWxlcgo8PCAvU2l6ZSA2IC9Sb290IDEgMCBSID4%2BCnN0YXJ0eHJlZgo0OTUKJSVFT0YK" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileContent": "JVBERi0xLjQKMSAwIG9iago8PCAvVHlwZSAvQ2F0YWxvZyAvUGFnZXMgMiAwIFIgPj4KZW5kb2JqCjIgMCBvYmoKPDwgL1R5cGUgL1BhZ2VzIC9LaWRzIFszIDAgUl0gL0NvdW50IDEgPj4KZW5kb2JqCjMgMCBvYmoKPDwgL1R5cGUgL1BhZ2UgL1BhcmVudCAyIDAgUiAvTWVkaWFCb3ggWzAgMCA2MTIgNzkyXSAvUmVzb3VyY2VzIDw8IC9Gb250IDw8IC9GMSA0IDAgUiA+PiA+PiAvQ29udGVudHMgNSAwIFIgPj4KZW5kb2JqCjQgMCBvYmoKPDwgL1R5cGUgL0ZvbnQgL1N1YnR5cGUgL1R5cGUxIC9CYXNlRm9udCAvSGVsdmV0aWNhID4+CmVuZG9iago1IDAgb2JqCjw8IC9MZW5ndGggMTM0ID4+CnN0cmVhbQpCVAovRjEgMTggVGYKNzIgNzIwIFRkCihBcXVhZm9yZXN0IHJ1bnRpbWUgdmVyaWZpY2F0aW9uKSBUagowIC0yNCBUZAooSW52b2ljZSBOdW1iZXI6IElOVi0xMjM0NSkgVGoKMCAtMjQgVGQKKFRvdGFsOiA0Mi4wMCBVU0QpIFRqCkVUCmVuZHN0cmVhbQplbmRvYmoKeHJlZgowIDYKMDAwMDAwMDAwMCA2NTUzNSBmIAowMDAwMDAwMDA5IDAwMDAwIG4gCjAwMDAwMDAwNTggMDAwMDAgbiAKMDAwMDAwMDExNSAwMDAwMCBuIAowMDAwMDAwMjQxIDAwMDAwIG4gCjAwMDAwMDAzMTEgMDAwMDAgbiAKdHJhaWxlcgo8PCAvU2l6ZSA2IC9Sb290IDEgMCBSID4+CnN0YXJ0eHJlZgo0OTUKJSVFT0YK"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aquaforestPDF/latest/actions/get-data-from-pdf?${params}`, {
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
| `fileContent` | file | yes | The content of the PDF file to extract data from. Default: `JVBERi0xLjQKMSAwIG9iago8PCAvVHlwZSAvQ2F0YWxvZyAvUGFnZXMgMiAwIFIgPj4KZW5kb2JqCjIgMCBvYmoKPDwgL1R5cGUgL1BhZ2VzIC9LaWRzIFszIDAgUl0gL0NvdW50IDEgPj4KZW5kb2JqCjMgMCBvYmoKPDwgL1R5cGUgL1BhZ2UgL1BhcmVudCAyIDAgUiAvTWVkaWFCb3ggWzAgMCA2MTIgNzkyXSAvUmVzb3VyY2VzIDw8IC9Gb250IDw8IC9GMSA0IDAgUiA+PiA+PiAvQ29udGVudHMgNSAwIFIgPj4KZW5kb2JqCjQgMCBvYmoKPDwgL1R5cGUgL0ZvbnQgL1N1YnR5cGUgL1R5cGUxIC9CYXNlRm9udCAvSGVsdmV0aWNhID4+CmVuZG9iago1IDAgb2JqCjw8IC9MZW5ndGggMTM0ID4+CnN0cmVhbQpCVAovRjEgMTggVGYKNzIgNzIwIFRkCihBcXVhZm9yZXN0IHJ1bnRpbWUgdmVyaWZpY2F0aW9uKSBUagowIC0yNCBUZAooSW52b2ljZSBOdW1iZXI6IElOVi0xMjM0NSkgVGoKMCAtMjQgVGQKKFRvdGFsOiA0Mi4wMCBVU0QpIFRqCkVUCmVuZHN0cmVhbQplbmRvYmoKeHJlZgowIDYKMDAwMDAwMDAwMCA2NTUzNSBmIAowMDAwMDAwMDA5IDAwMDAwIG4gCjAwMDAwMDAwNTggMDAwMDAgbiAKMDAwMDAwMDExNSAwMDAwMCBuIAowMDAwMDAwMjQxIDAwMDAwIG4gCjAwMDAwMDAzMTEgMDAwMDAgbiAKdHJhaWxlcgo8PCAvU2l6ZSA2IC9Sb290IDEgMCBSID4+CnN0YXJ0eHJlZgo0OTUKJSVFT0YK`. |
| `expectedKeys` | string | no | One key name per line to make values available to later actions without parsing JSON. Default: `Invoice Number\nTotal`. |
| `pageRange` | string | no | Page numbers to process, for example 1,3-4. Default: `1`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `pageLimit` | number | no | Maximum number of pages to process. Default: `1`. |
| `confidenceScore` | number | no | Filter out values below this confidence score. Aquaforest recommends starting from 0.5. Default: `0.5`. |
| `dateAsISO` | string | no | Date conversion format to return. Default: `ISO conversion (DMY input assumed)`. |
| `stripCurrencySymbol` | boolean | no | Remove currency symbols and strings before currency values are returned. Default: `false`. |
| `synonym` | boolean | no | Return keys that are synonyms of the expected key. Default: `true`. |
| `trimSymbols` | boolean | no | Remove leading and trailing symbols from keys before matching. Default: `true`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Aquaforest PDF API returns.

## Native endpoint

Through the native Aquaforest PDF API, this operation is `POST /GetPageData` (base URL `https://aquaforest-pdf.azure-api.net/AquaforestPDFAPIV2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-data-from-pdf.md) for the provider-specific parameters and requirements.

