# PDF.co: Get PDF Info

Retrieves PDF info from PDF.co.

```
GET https://connect.mindcloud.co/v1/universal/pDFco/latest/actions/get-pdf-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PDF.co `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pDFco/latest/actions/get-pdf-info?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pDFco/latest/actions/get-pdf-info?${params}`, {
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
| `url` | string | yes | URL of the PDF file to inspect. |
| `async` | boolean | no | Process info extraction as background job. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `password` | string | no | Password for protected PDFs. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "credits": 1,
      "duration": 1,
      "error": true,
      "info": {},
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
| `credits` | number | Credits consumed. |
| `duration` | number | Processing duration in ms. |
| `error` | boolean | Whether info extraction failed. |
| `info` | object | PDF metadata details including page count, title, author, and permissions. |
| `remainingCredits` | number | Credits left in account. |
| `status` | number | Status code from PDF.co. |

## Native endpoint

Through the native PDF.co API, this operation is `POST /pdf/info` (base URL `https://api.pdf.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-pdf-info.md) for the provider-specific parameters and requirements.

