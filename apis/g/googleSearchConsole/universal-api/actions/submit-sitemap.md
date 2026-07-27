# Google Search Console: Submit Sitemap



```
POST https://connect.mindcloud.co/v1/universal/googleSearchConsole/latest/actions/submit-sitemap
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Search Console `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/googleSearchConsole/latest/actions/submit-sitemap" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "siteUrl": "https://example.com",
  "feedpath": "https://www.example.com/sitemap.xml"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleSearchConsole/latest/actions/submit-sitemap', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "siteUrl": "https://example.com",
    "feedpath": "https://www.example.com/sitemap.xml"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `siteUrl` | list<string> | yes | The Search Console property URL that owns the sitemap. |
| `feedpath` | string | yes | The full URL of the sitemap to submit, for example https://www.example.com/sitemap.xml. Example: `https://www.example.com/sitemap.xml`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Google Search Console API returns.

## Native endpoint

Through the native Google Search Console API, this operation is `PUT sites/:siteUrl/sitemaps/:feedpath` (base URL `https://www.googleapis.com/webmasters/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/submit-sitemap.md) for the provider-specific parameters and requirements.

