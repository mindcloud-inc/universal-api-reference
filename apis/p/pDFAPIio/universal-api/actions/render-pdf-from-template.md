# PDF-API.io: Render PDF from Template

Creates a PDF document from a template in PDF-API.io.

```
POST https://connect.mindcloud.co/v1/universal/pDFAPIio/latest/actions/render-pdf-from-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PDF-API.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pDFAPIio/latest/actions/render-pdf-from-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateId": 1,
  "data": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pDFAPIio/latest/actions/render-pdf-from-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templateId": 1,
    "data": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `templateId` | list<number> | yes | The identifier of the template to use for generating the PDF. |
| `data` | object | yes | Key-value pairs representing the data to replace in the template. |
| `output` | list<string> | no | Optional output format for the generated PDF response. One of: `pdf`, `url`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | number | The HTTP-style status returned by PDF-API.io for the generated PDF request. |
| `url` | string | The temporary download URL for the generated PDF when output=url is used. |

## Native endpoint

Through the native PDF-API.io API, this operation is `POST /templates/:templateId/pdf` (base URL `https://pdf-api.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/render-pdf-from-template.md) for the provider-specific parameters and requirements.

