# Pling: List Content Categories

Retrieves public content categories from Pling.

```
GET https://connect.mindcloud.co/v1/universal/pling/latest/actions/list-content-categories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pling `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pling/latest/actions/list-content-categories?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pling/latest/actions/list-content-categories?${params}`, {
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
      "display_name": "Ava Chen",
      "id": "string",
      "name": "Ava Chen",
      "parent_id": "string",
      "xdg_type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `display_name` | string | Category display label. |
| `id` | string | Category identifier. |
| `name` | string | Category API name. |
| `parent_id` | string | Parent category identifier. |
| `xdg_type` | string | XDG category type. |

## Native endpoint

Through the native Pling API, this operation is `GET /content/categories` (base URL `https://api.pling.com/ocs/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-content-categories.md) for the provider-specific parameters and requirements.

