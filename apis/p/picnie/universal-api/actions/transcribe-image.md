# Picnie: Transcribe Image

Retrieves OCR text from an image in Picnie.

```
GET https://connect.mindcloud.co/v1/universal/picnie/latest/actions/transcribe-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Picnie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/picnie/latest/actions/transcribe-image?connectionId=$CONNECTION_ID&projectId=1&imageUrl=https%3A%2F%2Fexample.com&method=Original&language=Original" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "1",
  "imageUrl": "https://example.com",
  "method": "Original",
  "language": "Original"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/picnie/latest/actions/transcribe-image?${params}`, {
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
| `projectId` | number | yes | Project ID for the OCR operation. |
| `imageUrl` | string | yes | Image URL to transcribe. |
| `method` | string | yes | OCR method. The docs example uses Original. Default: `Original`. |
| `language` | string | yes | OCR language. The docs example uses Original. Default: `Original`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": true,
      "message": "string",
      "text": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error` | boolean |  |
| `message` | string |  |
| `text` | string |  |

## Native endpoint

Through the native Picnie API, this operation is `POST /transcribe-image` (base URL `https://picnie.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/transcribe-image.md) for the provider-specific parameters and requirements.

