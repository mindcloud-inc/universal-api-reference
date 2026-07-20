# ScrapeGraphAI: Get SmartScraper Status

Retrieves SmartScraper request status from ScrapeGraphAI.

```
GET https://connect.mindcloud.co/v1/universal/scrapeGraphAI/latest/actions/get-smartscraper-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapeGraphAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapeGraphAI/latest/actions/get-smartscraper-status?connectionId=$CONNECTION_ID&requestId=e5fc7d38-f30e-448d-8f39-347ef5aed0cb" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "requestId": "e5fc7d38-f30e-448d-8f39-347ef5aed0cb"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapeGraphAI/latest/actions/get-smartscraper-status?${params}`, {
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
| `requestId` | string | yes | SmartScraper request ID to retrieve. Example: `e5fc7d38-f30e-448d-8f39-347ef5aed0cb`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ScrapeGraphAI API returns.

## Native endpoint

Through the native ScrapeGraphAI API, this operation is `GET /smartscraper/:request_id` (base URL `https://api.scrapegraphai.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-smartscraper-status.md) for the provider-specific parameters and requirements.

