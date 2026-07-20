# HTML to PDF: Generate PDF from URL



```
POST https://connect.mindcloud.co/v1/universal/hTMLToPDF/latest/actions/generate-pdf-from-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HTML to PDF `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hTMLToPDF/latest/actions/generate-pdf-from-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com/report"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hTMLToPDF/latest/actions/generate-pdf-from-url', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com/report"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | Public URL whose rendered content should be converted into a PDF. Example: `https://example.com/report`. |
| `filename` | string | no | Optional filename to suggest for the generated PDF. Example: `report.pdf`. |
| `paperSize` | string | no | Optional paper size for the generated PDF. One of: `0`, `1`, `2`, `3`, `4`. |
| `orientation` | string | no | Optional page orientation for the generated PDF. One of: `0`, `1`. |
| `download` | boolean | no | When true, request a downloadable PDF response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        1
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<number> | PDF bytes returned by the provider. |
| `type` | string | Raw response type emitted by the runtime for the generated PDF payload. |

## Native endpoint

Through the native HTML to PDF API, this operation is `POST /pdf/generate` (base URL `https://platform.htmltopdfapi.co/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-pdf-from-url.md) for the provider-specific parameters and requirements.

