# TemplateFox: Create PDF

Creates a PDF from a template in TemplateFox.

```
POST https://connect.mindcloud.co/v1/universal/templateFox/latest/actions/create-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TemplateFox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/templateFox/latest/actions/create-pdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateId": "HMQywVpZxqAM",
  "data": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/templateFox/latest/actions/create-pdf', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templateId": "HMQywVpZxqAM",
    "data": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `templateId` | string | yes | Template short ID (12 characters). Example: `HMQywVpZxqAM`. |
| `data` | object | yes | Template data object. Keys must match template variables. Example: `[object Object]`. |
| `exportType` | string | no | Return a signed URL or raw PDF bytes. Example: `url`. |
| `expiration` | number | no | URL expiration in seconds when export type is url. Example: `86400`. |
| `filename` | string | no | Custom filename without the .pdf extension. Example: `invoice-001`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `storeS3` | boolean | no | Upload to your configured S3 bucket instead of the CDN. Example: `false`. |
| `s3Filepath` | string | no | Optional path prefix in your S3 bucket. Example: `generated/pdfs/`. |
| `s3Bucket` | string | no | Override the default configured S3 bucket. Example: `my-pdf-bucket`. |
| `pdfVariant` | string | no | Generate a standards-compliant PDF variant when needed. Example: `pdf/a-3b`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "credits_remaining": 1,
      "expires_in": 1,
      "filename": "Ava Chen",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `credits_remaining` | number |  |
| `expires_in` | number |  |
| `filename` | string |  |
| `url` | string |  |

## Native endpoint

Through the native TemplateFox API, this operation is `POST /v1/pdf/create` (base URL `https://api.templatefox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-pdf.md) for the provider-specific parameters and requirements.

