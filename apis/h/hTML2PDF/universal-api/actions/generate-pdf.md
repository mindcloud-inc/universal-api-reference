# HTML 2 PDF: Generate PDF



```
POST https://connect.mindcloud.co/v1/universal/hTML2PDF/latest/actions/generate-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HTML 2 PDF `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hTML2PDF/latest/actions/generate-pdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "html": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hTML2PDF/latest/actions/generate-pdf', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "html": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `html` | string | yes | HTML markup or a public URL to convert into a PDF document. |
| `format` | list | no | Optional paper format for the generated PDF. One of: `A0`, `A1`, `A2`, `A3`, `A4`, `A5`, `A6`, `Ledger`, `Legal`, `Letter`, `Tabloid`. |
| `landscape` | boolean | no | Render the pages in landscape orientation. |
| `filename` | string | no | Optional filename to suggest for the generated PDF. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `media` | list | no | Emulate the selected CSS media type while rendering. One of: `print`, `screen`. |
| `scale` | number | no | Rendering scale factor for the output PDF. |
| `width` | number | no | Custom page width for the generated PDF. |
| `height` | number | no | Custom page height for the generated PDF. |
| `waitFor` | number | no | Milliseconds to wait before rendering the page. |
| `callBackUrl` | string | no | Optional webhook URL to notify when PDF generation is complete. |
| `state` | string | no | State value returned unchanged to the callback URL. |
| `marginTop` | number | no | Top margin in pixels. |
| `marginRight` | number | no | Right margin in pixels. |
| `marginBottom` | number | no | Bottom margin in pixels. |
| `marginLeft` | number | no | Left margin in pixels. |
| `headerTemplate` | string | no | Optional HTML template rendered in the PDF header. |
| `footerTemplate` | string | no | Optional HTML template rendered in the PDF footer. |
| `userPassword` | string | no | User password required to open the generated PDF. |
| `ownerPassword` | string | no | Owner password used for PDF permission controls. |
| `permissions` | list<string> | no | Optional PDF permissions to allow when encryption is enabled. One of: `assemble`, `copy`, `edit`, `extract`, `fillform`, `modify`, `print`, `printbest`. Accepts multiple values as an array. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native HTML 2 PDF API returns.

## Native endpoint

Through the native HTML 2 PDF API, this operation is `POST /generate` (base URL `https://api.html2pdf.app/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-pdf.md) for the provider-specific parameters and requirements.

