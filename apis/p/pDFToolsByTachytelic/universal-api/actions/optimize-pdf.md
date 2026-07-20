# PDF Tools by Tachytelic: Optimize PDF



```
GET https://connect.mindcloud.co/v1/universal/pDFToolsByTachytelic/latest/actions/optimize-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PDF Tools by Tachytelic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pDFToolsByTachytelic/latest/actions/optimize-pdf?connectionId=$CONNECTION_ID&pdfFileContent=Base64%20PDF%20content" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pdfFileContent": "Base64 PDF content"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pDFToolsByTachytelic/latest/actions/optimize-pdf?${params}`, {
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
| `pdfFileContent` | string | yes | Base64-encoded PDF file content to optimize. Example: `Base64 PDF content`. |
| `mode` | list | no | Optimization mode: safe or aggressive. One of: `0`, `1`. Default: `safe`. |
| `garbage` | number | no | Unused object removal level from 0 to 4. Default: `1`. Example: `0-4`. |
| `deflate` | boolean | no | Whether to apply deflate compression to PDF streams. Default: `true`. |
| `clean` | boolean | no | Whether to clean and sanitize the PDF content. Default: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Clean": true,
      "Deflate": true,
      "Garbage": 1,
      "inputBytes": 1,
      "mode": "string",
      "OptimizedPdf": "string",
      "outputBytes": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Clean` | boolean | Whether document cleanup was applied. |
| `Deflate` | boolean | Whether deflate compression was applied. |
| `Garbage` | number | Garbage collection level applied by the API. |
| `inputBytes` | number | Original PDF size in bytes. |
| `mode` | string | Optimization mode applied by the API. |
| `OptimizedPdf` | string | Base64-encoded optimized PDF returned by Tachytelic. |
| `outputBytes` | number | Optimized PDF size in bytes. |

## Native endpoint

Through the native PDF Tools by Tachytelic API, this operation is `POST /optimize` (base URL `https://pdf.tachytelic.net/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/optimize-pdf.md) for the provider-specific parameters and requirements.

