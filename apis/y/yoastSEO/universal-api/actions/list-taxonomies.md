# Yoast SEO: List Taxonomies

Lists WordPress taxonomies.

```
GET https://connect.mindcloud.co/v1/universal/yoastSEO/latest/actions/list-taxonomies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yoast SEO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yoastSEO/latest/actions/list-taxonomies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yoastSEO/latest/actions/list-taxonomies?${params}`, {
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

Through the native Yoast SEO API, this operation is `GET /wp/v2/taxonomies` (base URL `{{credentials.siteUrl}}/wp-json`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-taxonomies.md) for the provider-specific parameters and requirements.

