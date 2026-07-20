# PDF.co: Classify Document

Classifies a document in PDF.co.

```
GET https://connect.mindcloud.co/v1/universal/pDFco/latest/actions/classify-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PDF.co `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pDFco/latest/actions/classify-document?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com%2Fdocument.pdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com/document.pdf"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pDFco/latest/actions/classify-document?${params}`, {
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
| `url` | string | yes | URL of PDF/image document to classify. Example: `https://example.com/document.pdf`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "body": {},
      "credits": 1,
      "duration": 1,
      "error": true,
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
| `body` | object |  |
| `credits` | number |  |
| `duration` | number |  |
| `error` | boolean |  |
| `pageCount` | number |  |
| `remainingCredits` | number |  |
| `status` | number |  |

## Native endpoint

Through the native PDF.co API, this operation is `POST /pdf/classifier` (base URL `https://api.pdf.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/classify-document.md) for the provider-specific parameters and requirements.

