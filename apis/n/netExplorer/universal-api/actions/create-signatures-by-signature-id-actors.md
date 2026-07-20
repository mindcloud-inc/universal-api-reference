# NetExplorer: Create Actor



```
POST https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/create-signatures-by-signature-id-actors
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetExplorer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/create-signatures-by-signature-id-actors" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "signatureId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/create-signatures-by-signature-id-actors', {
  method: 'POST',
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
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": 1,
      "lastName": "Chen",
      "link": "https://example.com",
      "phone": "string",
      "position": 1,
      "refuseAt": "2026-05-07T12:00:00.000Z",
      "refuseReason": "string",
      "signatureId": 1,
      "status": "string",
      "type": "string",
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
| `email` | string | Email de l'instance d'un acteur. |
| `firstName` | string | Prénom de l'instance d'un acteur. |
| `id` | number | Identifiant de l'instance d'un acteur |
| `lastName` | string | Nom de famille de l'instance d'un acteur. |
| `link` | string | Lien redirigeant vers la page externe de Yousign pour effecter l'action de signer ou d'approuver le flux de signature. |
| `phone` | string | Numéro de téléphone de l'instance d'un acteur. Dans un format internationnal. |
| `position` | number | Position de l'acteur dans le flux de la signature lorsqu'elle est séquencé |
| `refuseAt` | date | Date du refus de l'acteur pour une approbation ou pour une signature du flux de signature. |
| `refuseReason` | string | Raison de refus de l'acteur pour une approbation ou une signature du flux de signature. |
| `signatureId` | number | Identifiant de l'instance de signature lié à l'instance d'un acteur. |
| `status` | string | Status de l'instance d'un acteur au cour du flux de la signature. |
| `type` | string | Type de l'instance de l'instance d'un acteur (valeurs autorisées, 'signer', 'approver', 'follower'). |
| `userId` | number | Identifiant de l'utilisateur lié à cet acteur. |
| `yousignId` | string | Identifiant de l'instance de la signature côté Yousign. |

## Native endpoint

Through the native NetExplorer API, this operation is `POST /signatures/:signatureId/actors` (base URL `{{credentials.platformBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-signatures-by-signature-id-actors.md) for the provider-specific parameters and requirements.

