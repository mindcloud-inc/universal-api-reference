# ScrapeGraphAI: Get Markdownify Status

Retrieves Markdownify request status from ScrapeGraphAI.

```
GET https://connect.mindcloud.co/v1/universal/scrapeGraphAI/latest/actions/get-markdownify-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapeGraphAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapeGraphAI/latest/actions/get-markdownify-status?connectionId=$CONNECTION_ID&requestId=f1248013-7f30-46db-ab8a-484038415082" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "requestId": "f1248013-7f30-46db-ab8a-484038415082"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapeGraphAI/latest/actions/get-markdownify-status?${params}`, {
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
| `requestId` | string | yes | Markdownify request ID to retrieve. Example: `f1248013-7f30-46db-ab8a-484038415082`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ScrapeGraphAI API returns.

## Native endpoint

Through the native ScrapeGraphAI API, this operation is `GET /markdownify/:request_id` (base URL `https://api.scrapegraphai.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-markdownify-status.md) for the provider-specific parameters and requirements.

