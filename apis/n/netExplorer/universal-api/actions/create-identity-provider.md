# NetExplorer: Create Provider



```
POST https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/create-identity-provider
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetExplorer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/create-identity-provider" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/create-identity-provider', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "enable": true,
      "id": "string",
      "isAuthn": true,
      "isDirectory": true,
      "isSso": true,
      "matching": 1,
      "name": "Ava Chen",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `enable` | boolean | Indique si le fournisseur est actif ou non. |
| `id` | string | Identifiant unique du fournisseur. |
| `isAuthn` | boolean | Indique si le fournisseur permet de l'authentification directe depuis l'application. |
| `isDirectory` | boolean | Indique si le fournisseur d'identité permet l'accès à un annuaire d'utilisateurs/groupes (ex: LDAP) |
| `isSso` | boolean | Indique si le fournisseur propose de l'authentification unique (SSO). |
| `matching` | number | Indique quel type de matching est effectué entre les comptes du fournisseur d'identité et les comptes de la plateforme. Uniquement utilisé lors de la synchronisation initiale. |
| `name` | string | Nom du fournisseur tel qu'affiché dans la configuration et sur l'écran de connexion. |
| `type` | string | Type de fournisseur d'identité. |

## Native endpoint

Through the native NetExplorer API, this operation is `POST /identity/provider` (base URL `{{credentials.platformBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-identity-provider.md) for the provider-specific parameters and requirements.

