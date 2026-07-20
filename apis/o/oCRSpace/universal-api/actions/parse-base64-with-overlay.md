# OCRSpace: Parse Base64 With Overlay



```
GET https://connect.mindcloud.co/v1/universal/oCRSpace/latest/actions/parse-base64-with-overlay
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OCRSpace `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oCRSpace/latest/actions/parse-base64-with-overlay?connectionId=$CONNECTION_ID&base64Image=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "base64Image": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oCRSpace/latest/actions/parse-base64-with-overlay?${params}`, {
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
| `base64Image` | string | yes | Base64-encoded image or PDF input with its data URI prefix. |
| `language` | string | no | Three-letter OCR language code. Default: `eng`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "IsErroredOnProcessing": true,
      "OCRExitCode": 1,
      "ParsedResults": [
        {}
      ],
      "ProcessingTimeInMilliseconds": "string",
      "SearchablePDFURL": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `IsErroredOnProcessing` | boolean |  |
| `OCRExitCode` | number |  |
| `ParsedResults` | array<object> |  |
| `ProcessingTimeInMilliseconds` | string |  |
| `SearchablePDFURL` | string |  |

## Native endpoint

Through the native OCRSpace API, this operation is `POST /parse/image` (base URL `https://api.ocr.space`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/parse-base64-with-overlay.md) for the provider-specific parameters and requirements.

