# Nutrient - Convert to PDF: Convert URL File to PDF

Creates a PDF document from a file URL in Nutrient.

```
POST https://connect.mindcloud.co/v1/universal/nutrientConvertToPDF/latest/actions/convert-url-file-to-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nutrient - Convert to PDF `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/nutrientConvertToPDF/latest/actions/convert-url-file-to-pdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sourceUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nutrientConvertToPDF/latest/actions/convert-url-file-to-pdf', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sourceUrl": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sourceUrl` | string | yes | URL of the file to download and convert to PDF. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pdf": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pdf` | string | Generated PDF file returned by Nutrient. |

## Native endpoint

Through the native Nutrient - Convert to PDF API, this operation is `POST /build` (base URL `https://api.nutrient.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-url-file-to-pdf.md) for the provider-specific parameters and requirements.

