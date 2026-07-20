# CustomJS: Convert PDF to Text

Extracts text from a PDF in CustomJS.

```
GET https://connect.mindcloud.co/v1/universal/customJS/latest/actions/convert-pdf-to-text
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CustomJS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/customJS/latest/actions/convert-pdf-to-text?connectionId=$CONNECTION_ID&input.url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "input.url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/customJS/latest/actions/convert-pdf-to-text?${params}`, {
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
| `input.url` | string | yes | URL of the PDF file to convert to text. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "text": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `text` | string |  |

## Native endpoint

Through the native CustomJS API, this operation is `POST https://e.customjs.io/__js1-` (base URL `https://e.customjs.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-pdf-to-text.md) for the provider-specific parameters and requirements.

