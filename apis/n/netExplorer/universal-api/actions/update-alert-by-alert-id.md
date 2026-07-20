# NetExplorer: Update Alert



```
PUT https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/update-alert-by-alert-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetExplorer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/update-alert-by-alert-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "alertId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/update-alert-by-alert-id', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "alertId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `alertId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": 1,
      "expirationDate": "2026-05-07T12:00:00.000Z",
      "folderId": 1,
      "id": 1,
      "owner": "string",
      "ownerId": "string",
      "target": "string",
      "targetId": 1,
      "targetIsgroup": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | number | Identifiant numérique unique de l'objet Email utilisé pour l'envoi de l'alerte. |
| `expirationDate` | date | Date d'expiration de l'alerte. Après cette date, l'alerte existera toujours, mais sera considérée comme inactive. Le champs vaut null si aucune date d'expiration n'a été définie. |
| `folderId` | number | Identifiant numérique unique du dossier. |
| `id` | number | Identifiant numérique unique de l'alerte. |
| `owner` | string | Nom complet de l'utilisateur ayant créé l'alerte. |
| `ownerId` | string | Identifiant unique de l'utilisateur ayant créé l'alerte. |
| `target` | string | Nom complet de l'utilisateur cible, ou nom du groupe. |
| `targetId` | number | Identifiant unique de l'utilisateur ou du groupe alerté. |
| `targetIsgroup` | boolean | Indique si la cible est un utilisateur (true) ou un groupe (false). |

## Native endpoint

Through the native NetExplorer API, this operation is `PUT /alert/:alertId` (base URL `{{credentials.platformBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-alert-by-alert-id.md) for the provider-specific parameters and requirements.

