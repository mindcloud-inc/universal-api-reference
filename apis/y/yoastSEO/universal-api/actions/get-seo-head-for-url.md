# Yoast SEO: Get SEO Head For URL

Retrieves Yoast SEO metadata for a specific URL.

```
GET https://connect.mindcloud.co/v1/universal/yoastSEO/latest/actions/get-seo-head-for-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yoast SEO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yoastSEO/latest/actions/get-seo-head-for-url?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com%2Fexample-page" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com/example-page"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yoastSEO/latest/actions/get-seo-head-for-url?${params}`, {
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
| `url` | string | yes | Absolute URL to inspect for Yoast SEO metadata. Example: `https://example.com/example-page`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "html": "string",
      "json": {},
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `html` | string |  |
| `json` | object |  |
| `status` | number |  |

## Native endpoint

Through the native Yoast SEO API, this operation is `GET /yoast/v1/get_head` (base URL `{{credentials.siteUrl}}/wp-json`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-seo-head-for-url.md) for the provider-specific parameters and requirements.

