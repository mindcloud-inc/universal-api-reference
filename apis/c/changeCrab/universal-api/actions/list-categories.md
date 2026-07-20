# ChangeCrab: List Categories

Retrieves categories for a changelog from ChangeCrab.

```
GET https://connect.mindcloud.co/v1/universal/changeCrab/latest/actions/list-categories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChangeCrab `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/changeCrab/latest/actions/list-categories?connectionId=$CONNECTION_ID&id=e.g.%20product-updates" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "e.g. product-updates"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/changeCrab/latest/actions/list-categories?${params}`, {
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
| `id` | string | yes | The ChangeCrab changelog access ID. Example: `e.g. product-updates`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "colour": "string",
      "created_at": "string",
      "id": 1,
      "meta": "string",
      "project": "string",
      "title": "string",
      "type": "string",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `colour` | string |  |
| `created_at` | string |  |
| `id` | number |  |
| `meta` | string |  |
| `project` | string |  |
| `title` | string |  |
| `type` | string |  |
| `updated_at` | string |  |

## Native endpoint

Through the native ChangeCrab API, this operation is `GET /changelogs/:id/categories` (base URL `https://changecrab.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-categories.md) for the provider-specific parameters and requirements.

