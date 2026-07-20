# NetExplorer: Get Key



```
GET https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-ulink-key-by-ulink-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetExplorer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-ulink-key-by-ulink-key?connectionId=$CONNECTION_ID&ulinkKey=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ulinkKey": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-ulink-key-by-ulink-key?${params}`, {
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
| `ulinkKey` | string | yes |  |

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

Through the native NetExplorer API, this operation is `GET /ulink/key/:ulinkKey` (base URL `{{credentials.platformBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ulink-key-by-ulink-key.md) for the provider-specific parameters and requirements.

