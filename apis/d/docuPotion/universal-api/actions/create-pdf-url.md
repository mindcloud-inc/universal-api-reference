# DocuPotion: Create PDF URL



```
POST https://connect.mindcloud.co/v1/universal/docuPotion/latest/actions/create-pdf-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuPotion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docuPotion/latest/actions/create-pdf-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docuPotion/latest/actions/create-pdf-url', {
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
| `expiration` | number | no | How many minutes the generated URL should remain valid. Default: `60`. |
| `data` | object | no | Dynamic data that matches the variables in your template. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
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
| `expiresIn` | number | How many minutes the generated URL remains valid. |
| `format` | string | The generated file format. |
| `success` | boolean | Whether the request succeeded. |
| `url` | string | Presigned URL for the generated PDF. |

## Native endpoint

Through the native DocuPotion API, this operation is `POST /v1/create` (base URL `https://api.docupotion.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-pdf-url.md) for the provider-specific parameters and requirements.

