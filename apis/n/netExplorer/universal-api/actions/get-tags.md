# NetExplorer: List Tags



```
GET https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetExplorer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-tags?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-tags?${params}`, {
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
      "categoryId": 1,
      "color": "string",
      "id": 1,
      "key": "string",
      "name": "Ava Chen",
      "ownerId": 1,
      "private": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `categoryId` | number | Identifiant numérique de la catégorie de tag auquel est rattaché le tag |
| `color` | string | Nom de la couleur du tag |
| `id` | number | Identifiant numérique unique du tag |
| `key` | string | Nom du tag formaté pour la recherche |
| `name` | string | Nom du tag |
| `ownerId` | number | Identifiant de l'utilisateur qui a crée le tag |
| `private` | boolean | Détermine si le tag est privé ou non |

## Native endpoint

Through the native NetExplorer API, this operation is `GET /tags` (base URL `{{credentials.platformBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tags.md) for the provider-specific parameters and requirements.

