# CloudFill: Generate PDF

Generates a PDF from a CloudFill template.

```
POST https://connect.mindcloud.co/v1/universal/cloudFill/latest/actions/generate-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CloudFill `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cloudFill/latest/actions/generate-pdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "pdfKey": "pdf_abc123"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cloudFill/latest/actions/generate-pdf', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "pdfKey": "pdf_abc123"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `pdfKey` | string | yes | CloudFill PDF template key. Example: `pdf_abc123`. |
| `variables` | object | no | Map variable keys to replacement text values. Example: `[object Object]`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `images` | object | no | Map image field keys to public image URL objects. Example: `[object Object]`. |
| `flatten` | list<string> | no | Whether generated PDF form fields should be flattened. One of: `all`, `none`. Default: `all`. |
| `protectionPolicy` | object | no | Optional PDF protection policy settings. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `url` | string | Temporary URL to the generated PDF. |

## Native endpoint

Through the native CloudFill API, this operation is `POST /api/pdf/{pdfKey}/generate` (base URL `https://api.cloudfill.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-pdf.md) for the provider-specific parameters and requirements.

