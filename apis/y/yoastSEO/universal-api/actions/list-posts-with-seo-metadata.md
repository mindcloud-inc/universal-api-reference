# Yoast SEO: List Posts With SEO Metadata

Lists posts with Yoast SEO metadata.

```
GET https://connect.mindcloud.co/v1/universal/yoastSEO/latest/actions/list-posts-with-seo-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yoast SEO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yoastSEO/latest/actions/list-posts-with-seo-metadata?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yoastSEO/latest/actions/list-posts-with-seo-metadata?${params}`, {
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
| `search` | string | no | Limit results to posts matching a search string. Example: `seo`. |
| `slug` | string | no | Limit results to posts matching an exact slug. Example: `wordpress-seo`. |
| `perPage` | number | no | Maximum number of posts to return per page. Example: `10`. |
| `page` | number | no | Page number of results to return. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_links": {},
      "author": 1,
      "classList": [
        "string"
      ],
      "content": {},
      "date": "2026-05-07T12:00:00.000Z",
      "excerpt": {},
      "featuredMedia": 1,
      "id": 1,
      "link": "https://example.com",
      "meta": {},
      "modified": "2026-05-07T12:00:00.000Z",
      "slug": "string",
      "status": "string",
      "title": {},
      "type": "string",
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
| `author` | number |  |
| `classList` | array<string> |  |
| `content` | object |  |
| `date` | date |  |
| `excerpt` | object |  |
| `featuredMedia` | number |  |
| `id` | number |  |
| `link` | string |  |
| `meta` | object |  |
| `modified` | date |  |
| `slug` | string |  |
| `status` | string |  |
| `title` | object |  |
| `type` | string |  |
| `yoastHead` | string |  |
| `yoastHeadJson` | object |  |

## Native endpoint

Through the native Yoast SEO API, this operation is `GET /wp/v2/posts` (base URL `{{credentials.siteUrl}}/wp-json`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-posts-with-seo-metadata.md) for the provider-specific parameters and requirements.

