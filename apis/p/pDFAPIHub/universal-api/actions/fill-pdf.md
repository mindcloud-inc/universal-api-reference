# PDF API Hub: Fill PDF



```
POST https://connect.mindcloud.co/v1/universal/pDFAPIHub/latest/actions/fill-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PDF API Hub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pDFAPIHub/latest/actions/fill-pdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pDFAPIHub/latest/actions/fill-pdf', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templateId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `templateId` | string | yes | Template identifier for the PDF to fill. |
| `data` | object | no | Structured field values for detected template fields. |
| `formFields` | object | no | Values for PDF AcroForm fields. |
| `images` | object | no | Mapping of image field keys to public image URLs. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native PDF API Hub API returns.

## Native endpoint

Through the native PDF API Hub API, this operation is `POST /fill-pdf` (base URL `https://api.prefillpdf.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fill-pdf.md) for the provider-specific parameters and requirements.

