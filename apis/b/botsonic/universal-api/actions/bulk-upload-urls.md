# Botsonic: Bulk Upload URLs

Uploads multiple URLs as bot data in Botsonic.

```
POST https://connect.mindcloud.co/v1/universal/botsonic/latest/actions/bulk-upload-urls
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Botsonic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/botsonic/latest/actions/bulk-upload-urls" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "urls[]": "https://example.com/help/article"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/botsonic/latest/actions/bulk-upload-urls', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "urls[]": "https://example.com/help/article"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `urls[]` | array<string> | yes | URLs to upload or upsert for bot training. Example: `https://example.com/help/article`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sitemapId` | string | no | Optional sitemap identifier. Example: `sitemap_123`. |
| `isSitemap` | boolean | no | Whether the uploaded URLs represent a sitemap. Default: `false`. |
| `sitemapRoot` | string | no | Optional sitemap root URL. Example: `https://example.com/sitemap.xml`. |
| `abilityId` | string | no | Optional ability identifier. Example: `ability_123`. |
| `isCrawled` | boolean | no | Whether the URLs have already been crawled. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Botsonic API returns.

## Native endpoint

Through the native Botsonic API, this operation is `POST /v1/business/bot-data/bulk-upsert-urls` (base URL `https://api.botsonic.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-upload-urls.md) for the provider-specific parameters and requirements.

