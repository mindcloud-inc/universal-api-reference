# Yoast SEO Universal API Examples

These examples use the MindCloud API key and Yoast SEO connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Content Types With SEO Metadata

Lists content types with Yoast SEO metadata.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yoastSEO/latest/actions/list-content-types-with-seo-metadata?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yoastSEO/latest/actions/list-content-types-with-seo-metadata?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

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

See the full [List Content Types With SEO Metadata action reference](actions/list-content-types-with-seo-metadata.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/yoastSEO/latest/actions/list-content-types-with-seo-metadata).
