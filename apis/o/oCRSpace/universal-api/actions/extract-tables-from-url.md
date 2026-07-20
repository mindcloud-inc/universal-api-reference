# OCRSpace: Extract Tables From URL



```
GET https://connect.mindcloud.co/v1/universal/oCRSpace/latest/actions/extract-tables-from-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OCRSpace `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oCRSpace/latest/actions/extract-tables-from-url?connectionId=$CONNECTION_ID&url=https%3A%2F%2Focr.space%2FContent%2FImages%2Freceipt-ocr-original.jpg" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://ocr.space/Content/Images/receipt-ocr-original.jpg"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oCRSpace/latest/actions/extract-tables-from-url?${params}`, {
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
| `url` | string | yes | URL of the receipt or table image to parse. Default: `https://ocr.space/Content/Images/receipt-ocr-original.jpg`. |
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

Through the native OCRSpace API, this operation is `POST /parse/image` (base URL `https://api.ocr.space`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/extract-tables-from-url.md) for the provider-specific parameters and requirements.

