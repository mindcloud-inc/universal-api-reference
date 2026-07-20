# LLMLayer: Extract PDF Content

Retrieves extracted text from a PDF in LLMLayer.

```
GET https://connect.mindcloud.co/v1/universal/lLMLayer/latest/actions/extract-pdf-content
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LLMLayer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lLMLayer/latest/actions/extract-pdf-content?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com%2Fdocument.pdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com/document.pdf"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lLMLayer/latest/actions/extract-pdf-content?${params}`, {
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
| `url` | string | yes | PDF URL to process. Example: `https://example.com/document.pdf`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cost": 1,
      "pages": 1,
      "statusCode": 1,
      "text": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cost` | number | LLMLayer request cost. |
| `pages` | number | Number of pages processed. |
| `statusCode` | number | HTTP status code returned by the PDF fetch. |
| `text` | string | Extracted PDF text. |
| `url` | string | Processed PDF URL. |

## Native endpoint

Through the native LLMLayer API, this operation is `POST /api/v2/get_pdf_content` (base URL `https://api.llmlayer.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/extract-pdf-content.md) for the provider-specific parameters and requirements.

