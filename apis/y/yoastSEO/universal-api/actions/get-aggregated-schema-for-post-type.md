# Yoast SEO: Get Aggregated Schema For Post Type

Retrieves aggregated schema for a post type.

```
GET https://connect.mindcloud.co/v1/universal/yoastSEO/latest/actions/get-aggregated-schema-for-post-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yoast SEO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yoastSEO/latest/actions/get-aggregated-schema-for-post-type?connectionId=$CONNECTION_ID&postType=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "postType": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yoastSEO/latest/actions/get-aggregated-schema-for-post-type?${params}`, {
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
| `postType` | string | yes | Post type slug to aggregate, such as post, page, or product. |
| `page` | number | no | Schema aggregation page number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "rawBody": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `rawBody` | string | Raw newline-delimited JSON-LD returned by the schema aggregator endpoint. |

## Native endpoint

Through the native Yoast SEO API, this operation is `GET /yoast/v1/schema-aggregator/get-schema/:postType/:page` (base URL `{{credentials.siteUrl}}/wp-json`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-aggregated-schema-for-post-type.md) for the provider-specific parameters and requirements.

