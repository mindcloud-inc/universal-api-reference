# Yoast SEO: Get Content Type SEO Metadata

Retrieves Yoast SEO metadata for a content type archive.

```
GET https://connect.mindcloud.co/v1/universal/yoastSEO/latest/actions/get-content-type-seo-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yoast SEO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yoastSEO/latest/actions/get-content-type-seo-metadata?connectionId=$CONNECTION_ID&type=post" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "type": "post"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yoastSEO/latest/actions/get-content-type-seo-metadata?${params}`, {
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
| `type` | string | yes | WordPress post type key, for example post or page. Example: `post`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_links": {},
      "description": "string",
      "hierarchical": true,
      "icon": "string",
      "name": "Ava Chen",
      "restBase": "string",
      "restNamespace": "Ava Chen",
      "slug": "string",
      "taxonomies": [
        "string"
      ],
      "yoastHead": "string",
      "yoastHeadJson": {}
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
| `icon` | string |  |
| `name` | string |  |
| `restBase` | string |  |
| `restNamespace` | string |  |
| `slug` | string |  |
| `taxonomies` | array<string> |  |
| `yoastHead` | string |  |
| `yoastHeadJson` | object |  |

## Native endpoint

Through the native Yoast SEO API, this operation is `GET /wp/v2/types/:type` (base URL `{{credentials.siteUrl}}/wp-json`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-content-type-seo-metadata.md) for the provider-specific parameters and requirements.

