# Scrape do: Fetch webpage

Retrieves webpage content with Scrape do.

```
GET https://connect.mindcloud.co/v1/universal/scrapeDo/latest/actions/fetch-webpage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scrape do `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapeDo/latest/actions/fetch-webpage?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapeDo/latest/actions/fetch-webpage?${params}`, {
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
| `url` | string | yes | The target URL to fetch. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Scrape do API returns.

## Native endpoint

Through the native Scrape do API, this operation is `GET /` (base URL `https://api.scrape.do`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fetch-webpage.md) for the provider-specific parameters and requirements.

