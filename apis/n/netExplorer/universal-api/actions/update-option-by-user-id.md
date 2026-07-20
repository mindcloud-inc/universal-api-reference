# NetExplorer: Update Option



```
PUT https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/update-option-by-user-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetExplorer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/update-option-by-user-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/update-option-by-user-id', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "days": 1,
      "ips": "string",
      "target": "string",
      "targetId": "string",
      "targetIsgroup": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `days` | number | Masque numérique des jours de connexion autorisés. Il suffit d'additionner les valeurs, le résultat correspond au masque. Ex: Mardi + Jeudi = 4 + 16 = 20. ValeurJour 1Dimanche |
| `ips` | string | Liste blanche des IPs autorisées à se connecter à la plateforme. Attention Si un tableau vide est fourni au lieu de null, cet utilisateur ou ce groupe ne pourra pas se connecter. Cela peut être utilisé par exemple pour bloquer l'accès à un groupe complet. |
| `target` | string | Nom complet de l'utilisateur ou du groupe auquel s'applique les options. |
| `targetId` | string | Identifiant unique de l'utilisateur ou du groupe auquel s'applique les options. |
| `targetIsgroup` | boolean | Indique si la cible est un utilisateur ou un groupe. |

## Native endpoint

Through the native NetExplorer API, this operation is `PUT /option/:userId` (base URL `{{credentials.platformBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-option-by-user-id.md) for the provider-specific parameters and requirements.

