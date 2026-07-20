# NetExplorer: Get Category



```
GET https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-tag-categories-by-element-id-by-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetExplorer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-tag-categories-by-element-id-by-type?connectionId=$CONNECTION_ID&elementId=string&type=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "elementId": "string",
  "type": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-tag-categories-by-element-id-by-type?${params}`, {
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
| `elementId` | string | yes |  |
| `type` | string | yes |  |

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

Through the native NetExplorer API, this operation is `GET /tag/categories/:elementId/:type` (base URL `{{credentials.platformBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tag-categories-by-element-id-by-type.md) for the provider-specific parameters and requirements.

