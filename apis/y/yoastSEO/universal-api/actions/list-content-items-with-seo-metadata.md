# Yoast SEO: List Content Items With SEO Metadata

Lists content items with Yoast SEO metadata for a content type.

```
GET https://connect.mindcloud.co/v1/universal/yoastSEO/latest/actions/list-content-items-with-seo-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yoast SEO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yoastSEO/latest/actions/list-content-items-with-seo-metadata?connectionId=$CONNECTION_ID&contentType=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contentType": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yoastSEO/latest/actions/list-content-items-with-seo-metadata?${params}`, {
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
| `contentType` | string | yes | WordPress REST route for the content type, such as posts, pages, or a custom post type route. |
| `search` | string | no | Filter content items by a search string. |
| `slug` | string | no | Filter content items by slug. |
| `perPage` | number | no | Number of items to return per page. |
| `page` | number | no | Page number to return. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_links": {},
      "author": 1,
      "date": "string",
      "excerpt": {},
      "featuredMedia": 1,
      "id": 1,
      "link": "https://example.com",
      "menuOrder": 1,
      "meta": [
        "string"
      ],
      "parent": 1,
      "slug": "string",
      "status": "string",
      "template": "string",
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
| `date` | string |  |
| `excerpt` | object |  |
| `featuredMedia` | number |  |
| `id` | number |  |
| `link` | string |  |
| `menuOrder` | number |  |
| `meta` | array<string> |  |
| `parent` | number |  |
| `slug` | string |  |
| `status` | string |  |
| `template` | string |  |
| `title` | object |  |
| `type` | string |  |
| `yoastHead` | string |  |
| `yoastHeadJson` | object |  |

## Native endpoint

Through the native Yoast SEO API, this operation is `GET /wp/v2/:contentType` (base URL `{{credentials.siteUrl}}/wp-json`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-content-items-with-seo-metadata.md) for the provider-specific parameters and requirements.

