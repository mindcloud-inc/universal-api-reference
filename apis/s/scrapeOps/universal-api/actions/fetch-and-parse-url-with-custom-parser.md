# ScrapeOps: Fetch And Parse Url With Custom Parser

Fetches and parses a URL with a ScrapeOps custom parser.

```
GET https://connect.mindcloud.co/v1/universal/scrapeOps/latest/actions/fetch-and-parse-url-with-custom-parser
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapeOps `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapeOps/latest/actions/fetch-and-parse-url-with-custom-parser?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com&customParserId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com",
  "customParserId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapeOps/latest/actions/fetch-and-parse-url-with-custom-parser?${params}`, {
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
| `url` | string | yes | The URL to fetch and parse with the selected custom parser. |
| `customParserId` | string | yes | The ScrapeOps custom parser ID created in the ScrapeOps app. |
| `renderJs` | boolean | no | Enable JavaScript rendering for the target page before parsing. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ScrapeOps API returns.

## Native endpoint

Through the native ScrapeOps API, this operation is `GET https://proxy.scrapeops.io/v1/` (base URL `http://headers.scrapeops.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fetch-and-parse-url-with-custom-parser.md) for the provider-specific parameters and requirements.

