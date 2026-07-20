# Nutrient Document Web Services: Convert to PDF

Creates a PDF document in Nutrient Document Web Services API.

```
POST https://connect.mindcloud.co/v1/universal/nutrientDocumentWebServicesAPI/latest/actions/convert-to-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nutrient Document Web Services `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/nutrientDocumentWebServicesAPI/latest/actions/convert-to-pdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nutrientDocumentWebServicesAPI/latest/actions/convert-to-pdf', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | no | Public file URL to convert. |
| `file` | file | no | File to upload for conversion. |
| `password` | string | no | Password for protected source files. |
| `layout` | object | no | Layout settings for the generated PDF. |
| `pages` | object | no | Page range to include. |
| `contentType` | string | no | MIME type of the source file URL. |
| `markupMode` | string | no | Markup conversion mode. |
| `data` | object | no | Multipart request metadata. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Nutrient Document Web Services API returns.

## Native endpoint

Through the native Nutrient Document Web Services API, this operation is `POST /processor/convert_to_pdf` (base URL `https://api.nutrient.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-to-pdf.md) for the provider-specific parameters and requirements.

