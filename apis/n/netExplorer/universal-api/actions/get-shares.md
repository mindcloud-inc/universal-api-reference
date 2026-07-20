# NetExplorer: List Shares



```
GET https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-shares
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetExplorer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-shares?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-shares?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "flags": 1,
      "id": 1,
      "key": "string",
      "roots": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `flags` | number | Masque numérique des droits appliqués au lien. Valeur numériqueDroit 1Téléchargement uniquement |
| `id` | number | Identifiant numérique unique du partage par lien. |
| `key` | string | Clé de téléchargement du partage par lien. |
| `roots` | array<object> | Liste d'objets Contenu de partage. |

## Native endpoint

Through the native NetExplorer API, this operation is `GET /shares` (base URL `{{credentials.platformBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-shares.md) for the provider-specific parameters and requirements.

