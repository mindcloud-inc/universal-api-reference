# Yoast SEO: Get Schema Aggregator Sitemap XML

Retrieves the Schema Aggregator sitemap XML.

```
GET https://connect.mindcloud.co/v1/universal/yoastSEO/latest/actions/get-schema-aggregator-sitemap-xml
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yoast SEO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yoastSEO/latest/actions/get-schema-aggregator-sitemap-xml?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yoastSEO/latest/actions/get-schema-aggregator-sitemap-xml?${params}`, {
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
      "urlset": {},
      "xml": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `urlset` | object |  |
| `xml` | string |  |

## Native endpoint

Through the native Yoast SEO API, this operation is `GET /yoast/v1/schema-aggregator/get-xml` (base URL `{{credentials.siteUrl}}/wp-json`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-schema-aggregator-sitemap-xml.md) for the provider-specific parameters and requirements.

