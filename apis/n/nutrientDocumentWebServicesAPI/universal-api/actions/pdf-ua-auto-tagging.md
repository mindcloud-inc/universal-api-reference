# Nutrient Document Web Services: PDF/UA Auto-Tagging

Creates a PDF/UA document in Nutrient Document Web Services API.

```
POST https://connect.mindcloud.co/v1/universal/nutrientDocumentWebServicesAPI/latest/actions/pdf-ua-auto-tagging
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nutrient Document Web Services `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/nutrientDocumentWebServicesAPI/latest/actions/pdf-ua-auto-tagging" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nutrientDocumentWebServicesAPI/latest/actions/pdf-ua-auto-tagging', {
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
| `url` | string | no | Public PDF URL to convert to PDF/UA. |
| `file` | file | no | PDF file to convert to PDF/UA. |
| `password` | string | no | Password for protected PDF files. |
| `data` | object | no | Multipart request metadata. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Nutrient Document Web Services API returns.

## Native endpoint

Through the native Nutrient Document Web Services API, this operation is `POST /processor/pdfua` (base URL `https://api.nutrient.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/pdf-ua-auto-tagging.md) for the provider-specific parameters and requirements.

