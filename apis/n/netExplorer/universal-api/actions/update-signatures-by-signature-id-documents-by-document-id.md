# NetExplorer: Update Document



```
PUT https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/update-signatures-by-signature-id-documents-by-document-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetExplorer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/update-signatures-by-signature-id-documents-by-document-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "signatureId": "string",
  "documentId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/update-signatures-by-signature-id-documents-by-document-id', {
  method: 'PUT',
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
      "fields": {},
      "fileId": 1,
      "fileSignedId": 1,
      "id": 1,
      "initialPosition": "string",
      "name": "Ava Chen",
      "signatureId": 1,
      "yousignId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fields` | object | Tableau des champs de signature apposé sur l'instance du document. |
| `fileId` | number | Identifiant de l'instance du fichier lié à l'instance du document. |
| `fileSignedId` | number | Identifiant de l'instance du fichier signé lié à l'instance du document. |
| `id` | number | Identifiant de l'instance du document. |
| `initialPosition` | string | Position des paraphes sur l'instance du document (Valeurs autorisées, 'bottom-left', 'bottom-center', 'bottom-right'). |
| `name` | string | Nom de l'instance du document. |
| `signatureId` | number | Identifiant de l'instance de signature lié à l'instance du document. |
| `yousignId` | string | Identifiant Yousign de l'instance du document. |

## Native endpoint

Through the native NetExplorer API, this operation is `PATCH /signatures/:signatureId/documents/:documentId` (base URL `{{credentials.platformBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-signatures-by-signature-id-documents-by-document-id.md) for the provider-specific parameters and requirements.

