# NetExplorer: Create Field



```
POST https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/create-signatures-by-signature-id-documents-by-document-id-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetExplorer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/create-signatures-by-signature-id-documents-by-document-id-fields" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "signatureId": "string",
  "documentId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/create-signatures-by-signature-id-documents-by-document-id-fields', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "signatureId": "string",
    "documentId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `signatureId` | string | yes |  |
| `documentId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "height": 1,
      "page": 1,
      "signerId": "string",
      "type": "string",
      "width": 1,
      "x": 1,
      "y": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `height` | number |  |
| `page` | number |  |
| `signerId` | string |  |
| `type` | string |  |
| `width` | number |  |
| `x` | number |  |
| `y` | number |  |

## Native endpoint

Through the native NetExplorer API, this operation is `POST /signatures/:signatureId/documents/:documentId/fields` (base URL `{{credentials.platformBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-signatures-by-signature-id-documents-by-document-id-fields.md) for the provider-specific parameters and requirements.

