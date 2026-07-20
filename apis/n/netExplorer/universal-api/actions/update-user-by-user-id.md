# NetExplorer: Update User



```
PUT https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/update-user-by-user-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetExplorer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/update-user-by-user-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/update-user-by-user-id', {
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
      "active": true,
      "email": "ava@example.com",
      "firstname": "Ava",
      "id": "string",
      "language": "string",
      "lastname": "Chen",
      "login": "string",
      "organization": "string",
      "phone": "string",
      "roots": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean | Indique si le compte de l'utilisateur est actif ou non. |
| `email` | string | Adresses emails de l'utilisateur, séparées par des virgules. |
| `firstname` | string | Nom de l'utilisateur. |
| `id` | string | Identifiant unique de l'utilisateur. |
| `language` | string | Langue utilisée par la plateforme web pour traduire les labels de langue. Par défaut, la valeur auto permet de choisir la langue en fonction de celle du navigateur. Sinon, 6 langues sont disponibles : Code langueLangue frFrançais |
| `lastname` | string | Prénom de l'utilisateur. |
| `login` | string | Identifiant de l'utilisateur. |
| `organization` | string | Nom de la société dont fait partie l'utilisateur. Attention En fonction de la configuration de la plateforme, un groupe sera créé et portera ce nom. L'utilisateur y sera ensuite automatiquement ajouté. |
| `phone` | string | Liste des numéros de téléphones de l'utilisateur, séparés par des virgules. Ce champs n'a aucune utilité au sein de NetExplorer, mais peut être utilisé par des applicatifs tiers via l'API. |
| `roots` | number | Liste des identifiants numériques uniques des dossiers racines de l'utilisateur. Utilisé pour constituer son arborescence de base. |

## Native endpoint

Through the native NetExplorer API, this operation is `PUT /user/:userId` (base URL `{{credentials.platformBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-user-by-user-id.md) for the provider-specific parameters and requirements.

