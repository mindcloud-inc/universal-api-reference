# Yoast SEO: Get Content Item SEO Metadata

Retrieves Yoast SEO metadata for a content item.

```
GET https://connect.mindcloud.co/v1/universal/yoastSEO/latest/actions/get-content-item-seo-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yoast SEO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yoastSEO/latest/actions/get-content-item-seo-metadata?connectionId=$CONNECTION_ID&contentType=string&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contentType": "string",
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yoastSEO/latest/actions/get-content-item-seo-metadata?${params}`, {
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
| `id` | number | yes | Numeric ID of the content item to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_links": {},
      "author": 1,
      "content": {},
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
| `content` | object |  |
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

Through the native Yoast SEO API, this operation is `GET /wp/v2/:contentType/:id` (base URL `{{credentials.siteUrl}}/wp-json`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-content-item-seo-metadata.md) for the provider-specific parameters and requirements.

