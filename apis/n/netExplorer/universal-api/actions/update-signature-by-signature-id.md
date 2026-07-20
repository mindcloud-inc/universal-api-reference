# NetExplorer: Update Signature



```
PUT https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/update-signature-by-signature-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetExplorer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/update-signature-by-signature-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "signatureId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/update-signature-by-signature-id', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "signatureId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `signatureId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actors": "string",
      "deletedAt": "2026-05-07T12:00:00.000Z",
      "documents": "string",
      "expirationDate": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "isMasses": 1,
      "level": "string",
      "mode": "string",
      "name": "Ava Chen",
      "ordered": 1,
      "reminderDay": 1,
      "signatureParentId": 1,
      "status": "string",
      "userId": 1,
      "yousignId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actors` | string | Liste des acteurs lié à l'instance de la signature. |
| `deletedAt` | date | Date d'annulation de l'instance de la signature. |
| `documents` | string | Liste des documents lié à l'instande de la signature. |
| `expirationDate` | date | Date d'expiration de la l'instance de la signature |
| `id` | number | Identifiant de l'instance de la signature. |
| `isMasses` | number | Détermine si linstance de la signature est une signature de masse ou non (0 -> non, 1 -> oui). |
| `level` | string | Niveau de l'instance de la signature (valeurs autorisées, 'electronic_signature', 'advanced_electronic_signature', 'qualified_electronic_signature'). |
| `mode` | string | Mode de l'instance de la signature ('standard', 'parallel', 'mass'). |
| `name` | string | Nom de l'instance de signature. |
| `ordered` | number | Détermine si l'instance de la signature est ordonnée ou non (0 -> non, 1 -> oui). |
| `reminderDay` | number | Itervale de jour entre les relances automatique par mail de l'instance de la signature. |
| `signatureParentId` | number | Identifiant de l'instance de la signature parent, dans le cas de signature de masse. |
| `status` | string | Status actuel de l'instance de signature. |
| `userId` | number | Identifiant de l'instance de l'utilisateur initiateur de la signature. |
| `yousignId` | string | Identifiant de l'instance de la signature côté Yousign. |

## Native endpoint

Through the native NetExplorer API, this operation is `PATCH /signature/:signatureId` (base URL `{{credentials.platformBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-signature-by-signature-id.md) for the provider-specific parameters and requirements.

