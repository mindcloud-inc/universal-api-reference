# ScrapeGraphAI: Get SearchScraper Status

Retrieves SearchScraper request status from ScrapeGraphAI.

```
GET https://connect.mindcloud.co/v1/universal/scrapeGraphAI/latest/actions/get-searchscraper-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapeGraphAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapeGraphAI/latest/actions/get-searchscraper-status?connectionId=$CONNECTION_ID&requestId=f5893785-86dc-49d2-a77d-114f348b2968" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "requestId": "f5893785-86dc-49d2-a77d-114f348b2968"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapeGraphAI/latest/actions/get-searchscraper-status?${params}`, {
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
| `requestId` | string | yes | SearchScraper request ID to retrieve. Example: `f5893785-86dc-49d2-a77d-114f348b2968`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ScrapeGraphAI API returns.

## Native endpoint

Through the native ScrapeGraphAI API, this operation is `GET /searchscraper/:request_id` (base URL `https://api.scrapegraphai.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-searchscraper-status.md) for the provider-specific parameters and requirements.

