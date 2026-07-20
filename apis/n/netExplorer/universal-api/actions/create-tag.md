# NetExplorer: Create Tag



```
POST https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/create-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetExplorer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/create-tag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/create-tag', {
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

Through the native NetExplorer API, this operation is `POST /tag` (base URL `{{credentials.platformBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-tag.md) for the provider-specific parameters and requirements.

