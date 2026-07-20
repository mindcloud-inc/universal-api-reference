# PDF Tools by Tachytelic: Split PDF



```
GET https://connect.mindcloud.co/v1/universal/pDFToolsByTachytelic/latest/actions/split-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PDF Tools by Tachytelic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pDFToolsByTachytelic/latest/actions/split-pdf?connectionId=$CONNECTION_ID&pdfFileContent=Base64%20PDF%20content&splitType=NumberOfPages" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pdfFileContent": "Base64 PDF content",
  "splitType": "NumberOfPages"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pDFToolsByTachytelic/latest/actions/split-pdf?${params}`, {
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
| `pdfFileContent` | string | yes | Base64-encoded PDF file content. Example: `Base64 PDF content`. |
| `splitType` | list | yes | How to split the PDF: NumberOfPages or SpecifiedRanges. One of: `0`, `1`. Default: `NumberOfPages`. |
| `pagesPerSplit` | number | no | Number of pages per output file when Split Type is NumberOfPages. Default: `1`. Example: `1`. |
| `pageRanges` | string | no | Page ranges to split by when Split Type is SpecifiedRanges, for example 1-2,4. Example: `1-2,4`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "SplitPdfs": [
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
| `SplitPdfs` | array<string> | Base64-encoded PDF files produced by the split operation. |

## Native endpoint

Through the native PDF Tools by Tachytelic API, this operation is `POST /split` (base URL `https://pdf.tachytelic.net/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/split-pdf.md) for the provider-specific parameters and requirements.

