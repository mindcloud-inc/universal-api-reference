# NetExplorer: Update Category



```
PUT https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/update-tag-category-by-category-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetExplorer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/update-tag-category-by-category-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "categoryId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/update-tag-category-by-category-id', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "categoryId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `categoryId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "color": "string",
      "id": 1,
      "name": "Ava Chen",
      "nbTags": 1,
      "primaryColor": "string",
      "secondaryColor": "string",
      "tags": "string",
      "tertiaryColor": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string | Nom de la couleur de la catégorie |
| `id` | number | Identifiant numérique unique de la catégorie |
| `name` | string | Nom de la catégorie |
| `nbTags` | number | Nombre de tag présent dans la catégorie |
| `primaryColor` | string | Code couleur primaire de la catégorie (code HEX) |
| `secondaryColor` | string | Code couleur secondaire de la catégorie (code HEX) |
| `tags` | string | Contient les tags de la catégorie[ // Objets Tag { "id": 1, "name": "un tag", ... }, ... ] |
| `tertiaryColor` | string | Code couleur tertiaire de la catégorie (code HEX) |

## Native endpoint

Through the native NetExplorer API, this operation is `PUT /tag/category/:categoryId` (base URL `{{credentials.platformBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-tag-category-by-category-id.md) for the provider-specific parameters and requirements.

