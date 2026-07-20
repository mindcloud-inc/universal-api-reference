# PDF.co: Find Text in PDF

Finds text in a PDF in PDF.co.

```
GET https://connect.mindcloud.co/v1/universal/pDFco/latest/actions/find-text-in-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PDF.co `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pDFco/latest/actions/find-text-in-pdf?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fpdfco-test-files.s3.us-west-2.amazonaws.com%2Fpdf-find%2Fsample.pdf&searchString=invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://pdfco-test-files.s3.us-west-2.amazonaws.com/pdf-find/sample.pdf",
  "searchString": "invoice"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pDFco/latest/actions/find-text-in-pdf?${params}`, {
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
| `url` | string | yes | Source PDF URL accessible by PDF.co. Example: `https://pdfco-test-files.s3.us-west-2.amazonaws.com/pdf-find/sample.pdf`. |
| `searchString` | string | yes | Text to search for in the PDF. Example: `invoice`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `async` | boolean | no | Set true to run as async job. Example: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "body": [
        {}
      ],
      "credits": 1,
      "duration": 1,
      "error": true,
      "name": "Ava Chen",
      "pageCount": 1,
      "remainingCredits": 1,
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `body` | array<object> |  |
| `credits` | number |  |
| `duration` | number |  |
| `error` | boolean |  |
| `name` | string |  |
| `pageCount` | number |  |
| `remainingCredits` | number |  |
| `status` | number |  |

## Native endpoint

Through the native PDF.co API, this operation is `POST /pdf/find` (base URL `https://api.pdf.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-text-in-pdf.md) for the provider-specific parameters and requirements.

