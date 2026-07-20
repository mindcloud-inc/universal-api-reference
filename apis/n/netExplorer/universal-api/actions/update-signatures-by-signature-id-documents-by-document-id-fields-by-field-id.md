# NetExplorer: Update Field



```
PUT https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/update-signatures-by-signature-id-documents-by-document-id-fields-by-field-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetExplorer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/update-signatures-by-signature-id-documents-by-document-id-fields-by-field-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "signatureId": "string",
  "documentId": "string",
  "fieldId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/update-signatures-by-signature-id-documents-by-document-id-fields-by-field-id', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "signatureId": "string",
    "documentId": "string",
    "fieldId": "string"
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
| `fieldId` | string | yes |  |

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

Through the native NetExplorer API, this operation is `PATCH /signatures/:signatureId/documents/:documentId/fields/:fieldId` (base URL `{{credentials.platformBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-signatures-by-signature-id-documents-by-document-id-fields-by-field-id.md) for the provider-specific parameters and requirements.

