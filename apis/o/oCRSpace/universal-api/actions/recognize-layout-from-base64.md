# OCRSpace: Recognize Layout From Base64



```
GET https://connect.mindcloud.co/v1/universal/oCRSpace/latest/actions/recognize-layout-from-base64
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OCRSpace `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oCRSpace/latest/actions/recognize-layout-from-base64?connectionId=$CONNECTION_ID&base64Image=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "base64Image": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oCRSpace/latest/actions/recognize-layout-from-base64?${params}`, {
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
      "ProcessingTimeInMilliseconds": "string"
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

## Native endpoint

Through the native OCRSpace API, this operation is `POST /parse/image` (base URL `https://api.ocr.space`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/recognize-layout-from-base64.md) for the provider-specific parameters and requirements.

