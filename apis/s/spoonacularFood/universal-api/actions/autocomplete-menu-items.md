# Spoonacular Food: Autocomplete Menu Items

Finds menu item suggestions in Spoonacular Food by partial name.

```
GET https://connect.mindcloud.co/v1/universal/spoonacularFood/latest/actions/autocomplete-menu-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Spoonacular Food `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/spoonacularFood/latest/actions/autocomplete-menu-items?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/spoonacularFood/latest/actions/autocomplete-menu-items?${params}`, {
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
| `query` | string | yes | Menu item name prefix to autocomplete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `title` | string |  |

## Native endpoint

Through the native Spoonacular Food API, this operation is `GET /food/menuItems/suggest` (base URL `https://api.spoonacular.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/autocomplete-menu-items.md) for the provider-specific parameters and requirements.

