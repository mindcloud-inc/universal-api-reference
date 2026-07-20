# Longreads: Get Post Type Index

Retrieves post type definitions from Longreads.

```
GET https://connect.mindcloud.co/v1/universal/longreads/latest/actions/get-post-type-index
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Longreads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/longreads/latest/actions/get-post-type-index?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/longreads/latest/actions/get-post-type-index?${params}`, {
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
      "description": "string",
      "hierarchical": true,
      "name": "Ava Chen",
      "rest_base": "string",
      "slug": "string",
      "viewable": true,
      "visibility": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `hierarchical` | boolean |  |
| `name` | string |  |
| `rest_base` | string |  |
| `slug` | string |  |
| `viewable` | boolean |  |
| `visibility` | object |  |

## Native endpoint

Through the native Longreads API, this operation is `GET /wp/v2/types` (base URL `https://longreads.com/wp-json`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-post-type-index.md) for the provider-specific parameters and requirements.

