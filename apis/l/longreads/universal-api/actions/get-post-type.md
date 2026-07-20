# Longreads: Get Post Type

Retrieves a post type definition from Longreads.

```
GET https://connect.mindcloud.co/v1/universal/longreads/latest/actions/get-post-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Longreads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/longreads/latest/actions/get-post-type?connectionId=$CONNECTION_ID&type=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "type": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/longreads/latest/actions/get-post-type?${params}`, {
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
| `type` | string | yes | The post type slug to retrieve, such as post. |

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

Through the native Longreads API, this operation is `GET /wp/v2/types/{type}` (base URL `https://longreads.com/wp-json`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-post-type.md) for the provider-specific parameters and requirements.

