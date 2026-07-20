# Biyo POS: List Categories

Retrieves category records from Biyo POS.

```
GET https://connect.mindcloud.co/v1/universal/biyoPOS/latest/actions/list-categories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Biyo POS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/biyoPOS/latest/actions/list-categories?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/biyoPOS/latest/actions/list-categories?${params}`, {
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
      "active": true,
      "archived": true,
      "color": 1,
      "description": "string",
      "id": 1,
      "image": "string",
      "name": "Ava Chen",
      "parent": {},
      "sorting": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `archived` | boolean |  |
| `color` | number |  |
| `description` | string |  |
| `id` | number |  |
| `image` | string |  |
| `name` | string |  |
| `parent` | object |  |
| `sorting` | number |  |

## Native endpoint

Through the native Biyo POS API, this operation is `GET /api/v1/categories/` (base URL `https://mindcloud.biyo.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-categories.md) for the provider-specific parameters and requirements.

