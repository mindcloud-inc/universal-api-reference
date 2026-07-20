# SelectPdf: Extract Text from PDF URL



```
GET https://connect.mindcloud.co/v1/universal/selectPdf/latest/actions/extract-text-from-pdfurl
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SelectPdf `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/selectPdf/latest/actions/extract-text-from-pdfurl?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/selectPdf/latest/actions/extract-text-from-pdfurl?${params}`, {
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
| `url` | string | yes | The public PDF URL to process. |

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
| `text` | string | Extracted plain text content from the source PDF. |

## Native endpoint

Through the native SelectPdf API, this operation is `POST /pdftotext/` (base URL `https://selectpdf.com/api2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/extract-text-from-pdfurl.md) for the provider-specific parameters and requirements.

