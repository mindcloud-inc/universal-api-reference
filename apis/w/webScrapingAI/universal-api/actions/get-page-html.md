# WebScraping.AI: Get Page HTML



```
GET https://connect.mindcloud.co/v1/universal/webScrapingAI/latest/actions/get-page-html
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WebScraping.AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webScrapingAI/latest/actions/get-page-html?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webScrapingAI/latest/actions/get-page-html?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native WebScraping.AI API returns.

## Native endpoint

Through the native WebScraping.AI API, this operation is `GET /html` (base URL `https://api.webscraping.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-page-html.md) for the provider-specific parameters and requirements.

