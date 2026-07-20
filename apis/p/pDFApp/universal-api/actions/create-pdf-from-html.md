# PDF-app: Create PDF From HTML

Creates a PDF from HTML in PDF-app.

```
POST https://connect.mindcloud.co/v1/universal/pDFApp/latest/actions/create-pdf-from-html
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PDF-app `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pDFApp/latest/actions/create-pdf-from-html" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "htmlTemplate": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pDFApp/latest/actions/create-pdf-from-html', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "htmlTemplate": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `htmlTemplate` | string | yes | HTML content to render into a PDF. |
| `fileName` | string | no | Optional output file name. |
| `async` | boolean | no | Set true to queue the PDF generation asynchronously. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `format` | string | no | Optional paper format such as A4 or Letter. |
| `templateHtmlId` | string | no | Optional saved HTML template ID to reuse instead of sending raw HTML. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creditsConsumed": 1,
      "creditsRemaining": 1,
      "jobId": "string",
      "message": "string",
      "presignedUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creditsConsumed` | number | Credits consumed by the operation. |
| `creditsRemaining` | number | Remaining PDF-app credits after the operation. |
| `jobId` | string | Job identifier returned by PDF-app. |
| `message` | string | Provider success message. |
| `presignedUrl` | string | Temporary download URL for the generated PDF. |

## Native endpoint

Through the native PDF-app API, this operation is `POST /html_to_pdf` (base URL `https://api.pdf-app.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-pdf-from-html.md) for the provider-specific parameters and requirements.

