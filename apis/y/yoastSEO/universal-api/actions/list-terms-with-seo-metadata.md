# Yoast SEO: List Terms With SEO Metadata

Lists taxonomy terms with Yoast SEO metadata.

```
GET https://connect.mindcloud.co/v1/universal/yoastSEO/latest/actions/list-terms-with-seo-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yoast SEO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yoastSEO/latest/actions/list-terms-with-seo-metadata?connectionId=$CONNECTION_ID&taxonomyRoute=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taxonomyRoute": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yoastSEO/latest/actions/list-terms-with-seo-metadata?${params}`, {
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
| `taxonomyRoute` | string | yes | WordPress REST route for the taxonomy terms collection, such as categories or post_tag. |
| `search` | string | no | Filter terms by a search string. |
| `slug` | string | no | Filter terms by slug. |
| `perPage` | number | no | Number of terms to return per page. |
| `page` | number | no | Page number to return. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_links": {},
      "count": 1,
      "description": "string",
      "id": 1,
      "link": "https://example.com",
      "meta": [
        "string"
      ],
      "name": "Ava Chen",
      "parent": 1,
      "slug": "string",
      "taxonomy": "string",
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
| `count` | number |  |
| `description` | string |  |
| `id` | number |  |
| `link` | string |  |
| `meta` | array<string> |  |
| `name` | string |  |
| `parent` | number |  |
| `slug` | string |  |
| `taxonomy` | string |  |
| `yoastHead` | string |  |
| `yoastHeadJson` | object |  |

## Native endpoint

Through the native Yoast SEO API, this operation is `GET /wp/v2/:taxonomyRoute` (base URL `{{credentials.siteUrl}}/wp-json`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-terms-with-seo-metadata.md) for the provider-specific parameters and requirements.

