# ScraperAPI: Send Scrape Request

Retrieves a scraped response from ScraperAPI with a POST request.

```
GET https://connect.mindcloud.co/v1/universal/scraperAPI/latest/actions/send-scrape-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScraperAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scraperAPI/latest/actions/send-scrape-request?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scraperAPI/latest/actions/send-scrape-request?${params}`, {
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
| `url` | string | yes | The target URL to scrape. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ScraperAPI API returns.

## Native endpoint

Through the native ScraperAPI API, this operation is `POST https://api.scraperapi.com` (base URL `https://api.scraperapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-scrape-request.md) for the provider-specific parameters and requirements.

