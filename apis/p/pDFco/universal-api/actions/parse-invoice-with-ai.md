# PDF.co: Parse Invoice with AI

Parses an invoice with AI in PDF.co.

```
GET https://connect.mindcloud.co/v1/universal/pDFco/latest/actions/parse-invoice-with-ai
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PDF.co `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pDFco/latest/actions/parse-invoice-with-ai?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com%2Finvoice.pdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com/invoice.pdf"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pDFco/latest/actions/parse-invoice-with-ai?${params}`, {
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
| `url` | string | yes | URL of invoice PDF/image to parse. Example: `https://example.com/invoice.pdf`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "credits": 1,
      "duration": 1,
      "error": true,
      "jobId": "string",
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
| `credits` | number |  |
| `duration` | number |  |
| `error` | boolean |  |
| `jobId` | string |  |
| `remainingCredits` | number |  |
| `status` | number |  |

## Native endpoint

Through the native PDF.co API, this operation is `POST /ai-invoice-parser` (base URL `https://api.pdf.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/parse-invoice-with-ai.md) for the provider-specific parameters and requirements.

