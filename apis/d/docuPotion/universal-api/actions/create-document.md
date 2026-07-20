# DocuPotion: Create Document



```
POST https://connect.mindcloud.co/v1/universal/docuPotion/latest/actions/create-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuPotion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docuPotion/latest/actions/create-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docuPotion/latest/actions/create-document', {
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
| `templateId` | list<string> | yes | Choose the DocuPotion template to render. |
| `output` | list<string> | no | One of: `Base64`, `URL`. Default: `base64`. |
| `format` | list<string> | no | One of: `PDF`, `PNG`. Default: `pdf`. |
| `data` | object | no | Dynamic data that matches the variables in your template. Example: `[object Object]`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `expiration` | number | no | How many minutes the generated URL should remain valid when output is URL. Default: `60`. |
| `s3Bucket` | boolean | no | Upload the generated file to your connected S3 bucket instead of DocuPotion storage. Default: `false`. |
| `s3Key` | string | no | Custom S3 object key without the file extension. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "base64": "string",
      "expiresIn": 1,
      "format": "string",
      "success": true,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `base64` | string | Base64-encoded document content when output is base64. |
| `expiresIn` | number | How many minutes the generated URL remains valid when output is url. |
| `format` | string | The generated file format. |
| `success` | boolean | Whether the request succeeded. |
| `url` | string | Presigned URL when output is url. |

## Native endpoint

Through the native DocuPotion API, this operation is `POST /v1/create` (base URL `https://api.docupotion.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-document.md) for the provider-specific parameters and requirements.

