# Nutrient - Extract from PDF: Extract PDF Plain Text

Extracts plain text from a PDF with Nutrient.

```
GET https://connect.mindcloud.co/v1/universal/nutrientExtractFromPDF/latest/actions/extract-pdf-plain-text
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nutrient - Extract from PDF `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nutrientExtractFromPDF/latest/actions/extract-pdf-plain-text?connectionId=$CONNECTION_ID&document=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "document": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nutrientExtractFromPDF/latest/actions/extract-pdf-plain-text?${params}`, {
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
| `document` | file | yes | PDF file to extract plain text from. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pages": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pages` | array<object> | PDF pages with extracted plain text content. |

## Native endpoint

Through the native Nutrient - Extract from PDF API, this operation is `POST /build` (base URL `https://api.nutrient.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/extract-pdf-plain-text.md) for the provider-specific parameters and requirements.

