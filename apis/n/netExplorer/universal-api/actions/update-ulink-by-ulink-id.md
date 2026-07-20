# NetExplorer: Update Ulink



```
PUT https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/update-ulink-by-ulink-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetExplorer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/update-ulink-by-ulink-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "ulinkId": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/update-ulink-by-ulink-id', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "ulinkId": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ulinkId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "flags": 1,
      "folder": "string",
      "folderId": 1,
      "folderSize": 1,
      "id": 1,
      "isValid": true,
      "key": "string",
      "owner": "string",
      "ownerId": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `flags` | number | Masque numérique appliqués au lien. Valeur numériqueDroit 1Protégé par mot de passe |
| `folder` | string | Nom du dossier de destination. |
| `folderId` | number | Identifiant numérique unique du dossier dans lequel déposer les documents. Peut être défini à null si le dossier de destination n'existe plus. |
| `folderSize` | number | Taille du dossier de destination. |
| `id` | number | Identifiant numérique unique du lien de dépôt. |
| `isValid` | boolean | Indique si le lien de dépôt est toujours accessible. Pour cela, il ne doit pas être expiré et le dossier de destination doit être toujours présent. |
| `key` | string | Clé d'accès au lien de dépôt. |
| `owner` | string | Nom complet de l'utilisateur propriétaire du lien de dépôt. |
| `ownerId` | string | Identifiant unique de propriétaire. |
| `url` | string | URL vers le contenu du lien. |

## Native endpoint

Through the native NetExplorer API, this operation is `PUT /ulink/:ulinkId` (base URL `{{credentials.platformBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-ulink-by-ulink-id.md) for the provider-specific parameters and requirements.

