# OCRSpace: Detect Language From URL



```
GET https://connect.mindcloud.co/v1/universal/oCRSpace/latest/actions/detect-language-from-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OCRSpace `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oCRSpace/latest/actions/detect-language-from-url?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fdl.a9t9.com%2Focr%2Fsolarcell.jpg" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://dl.a9t9.com/ocr/solarcell.jpg"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oCRSpace/latest/actions/detect-language-from-url?${params}`, {
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
| `url` | string | yes | URL of the remote image or PDF to parse. Default: `https://dl.a9t9.com/ocr/solarcell.jpg`. |

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

Through the native OCRSpace API, this operation is `POST /parse/image` (base URL `https://api.ocr.space`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/detect-language-from-url.md) for the provider-specific parameters and requirements.

