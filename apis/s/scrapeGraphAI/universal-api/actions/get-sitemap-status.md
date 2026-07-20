# ScrapeGraphAI: Get Sitemap Status

Retrieves sitemap request status from ScrapeGraphAI.

```
GET https://connect.mindcloud.co/v1/universal/scrapeGraphAI/latest/actions/get-sitemap-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapeGraphAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapeGraphAI/latest/actions/get-sitemap-status?connectionId=$CONNECTION_ID&requestId=efb5b489-062a-4146-8453-1b1380e1edd7" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "requestId": "efb5b489-062a-4146-8453-1b1380e1edd7"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapeGraphAI/latest/actions/get-sitemap-status?${params}`, {
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
| `requestId` | string | yes | Sitemap request ID to retrieve. Example: `efb5b489-062a-4146-8453-1b1380e1edd7`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ScrapeGraphAI API returns.

## Native endpoint

Through the native ScrapeGraphAI API, this operation is `GET /sitemap/:request_id` (base URL `https://api.scrapegraphai.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sitemap-status.md) for the provider-specific parameters and requirements.

