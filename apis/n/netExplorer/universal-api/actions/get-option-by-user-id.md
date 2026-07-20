# NetExplorer: Get Option By User ID



```
GET https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-option-by-user-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetExplorer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-option-by-user-id?connectionId=$CONNECTION_ID&userId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-option-by-user-id?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

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

Through the native NetExplorer API, this operation is `GET /option/:userId` (base URL `{{credentials.platformBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-option-by-user-id.md) for the provider-specific parameters and requirements.

