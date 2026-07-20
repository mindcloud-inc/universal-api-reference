# 1001fx: Scrape HTML

Retrieves structured content from HTML or a website.

```
GET https://connect.mindcloud.co/v1/universal/fx/latest/actions/scrape-html
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 1001fx `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fx/latest/actions/scrape-html?connectionId=$CONNECTION_ID&selectors%5B%5D=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "selectors[]": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fx/latest/actions/scrape-html?${params}`, {
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
| `html` | string | no | HTML source to scrape. |
| `selectors[]` | array<object> | yes | Selectors that define what content to extract. |
| `url` | string | no | URL to scrape when not passing raw HTML. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native 1001fx API returns.

## Native endpoint

Through the native 1001fx API, this operation is `POST /data/scrapehtml` (base URL `https://api.1001fx.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/scrape-html.md) for the provider-specific parameters and requirements.

