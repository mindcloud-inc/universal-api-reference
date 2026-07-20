# Nutrient - Convert to PDF: Convert URL File to PDF/A

Creates a PDF/A document from a file URL in Nutrient.

```
POST https://connect.mindcloud.co/v1/universal/nutrientConvertToPDF/latest/actions/convert-url-file-to-pdfa
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nutrient - Convert to PDF `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/nutrientConvertToPDF/latest/actions/convert-url-file-to-pdfa" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sourceUrl": "https://example.com",
  "conformance": "pdfa-2a"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nutrientConvertToPDF/latest/actions/convert-url-file-to-pdfa', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sourceUrl": "https://example.com",
    "conformance": "pdfa-2a"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sourceUrl` | string | yes | URL of the file to convert to PDF/A. |
| `conformance` | list | yes | PDF/A conformance level for archival output. One of: `PDF/A-1b`, `PDF/A-2a`, `PDF/A-2b`, `PDF/A-3b`. Default: `pdfa-2a`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pdfa": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pdfa` | string | Generated PDF/A file returned by Nutrient. |

## Native endpoint

Through the native Nutrient - Convert to PDF API, this operation is `POST /build` (base URL `https://api.nutrient.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-url-file-to-pdfa.md) for the provider-specific parameters and requirements.

