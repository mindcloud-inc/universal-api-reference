# Diffbot: Search Crawl Or Bulk Job

Searches a Diffbot crawl or bulk job with DQL.

```
GET https://connect.mindcloud.co/v1/universal/diffbot/latest/actions/search-crawl-or-bulk-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Diffbot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/diffbot/latest/actions/search-crawl-or-bulk-job?connectionId=$CONNECTION_ID&collectionName=Ava%20Chen&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "collectionName": "Ava Chen",
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/diffbot/latest/actions/search-crawl-or-bulk-job?${params}`, {
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
| `collectionName` | string | yes | Bulk or crawl collection name to search. |
| `query` | string | yes | Search query to execute against the collection. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Diffbot API returns.

## Native endpoint

Through the native Diffbot API, this operation is `GET /v3/search/` (base URL `https://api.diffbot.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-crawl-or-bulk-job.md) for the provider-specific parameters and requirements.

