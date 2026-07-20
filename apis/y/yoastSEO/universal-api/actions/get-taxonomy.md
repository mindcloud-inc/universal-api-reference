# Yoast SEO: Get Taxonomy

Retrieves a WordPress taxonomy.

```
GET https://connect.mindcloud.co/v1/universal/yoastSEO/latest/actions/get-taxonomy
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yoast SEO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yoastSEO/latest/actions/get-taxonomy?connectionId=$CONNECTION_ID&taxonomy=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taxonomy": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yoastSEO/latest/actions/get-taxonomy?${params}`, {
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
| `taxonomy` | string | yes | Taxonomy slug to retrieve, such as category or post_tag. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_links": {},
      "description": "string",
      "hierarchical": true,
      "name": "Ava Chen",
      "restBase": "string",
      "restNamespace": "Ava Chen",
      "slug": "string",
      "types": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_links` | object |  |
| `description` | string |  |
| `hierarchical` | boolean |  |
| `name` | string |  |
| `restBase` | string |  |
| `restNamespace` | string |  |
| `slug` | string |  |
| `types` | array<string> |  |

## Native endpoint

Through the native Yoast SEO API, this operation is `GET /wp/v2/taxonomies/:taxonomy` (base URL `{{credentials.siteUrl}}/wp-json`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-taxonomy.md) for the provider-specific parameters and requirements.

