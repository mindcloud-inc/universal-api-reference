# NetExplorer: Create Document



```
POST https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/create-signatures-by-signature-id-documents-by-file-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetExplorer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/create-signatures-by-signature-id-documents-by-file-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "signatureId": "string",
  "fileId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/create-signatures-by-signature-id-documents-by-file-id', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "signatureId": "string",
    "fileId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `signatureId` | string | yes |  |
| `fileId` | string | yes |  |

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

Through the native NetExplorer API, this operation is `POST /signatures/:signatureId/documents/:fileId` (base URL `{{credentials.platformBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-signatures-by-signature-id-documents-by-file-id.md) for the provider-specific parameters and requirements.

