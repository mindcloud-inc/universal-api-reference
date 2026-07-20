# ScrapFly: List Crawled URLs

Retrieves crawled URLs from ScrapFly.

```
GET https://connect.mindcloud.co/v1/universal/scrapFly/latest/actions/list-crawled-ur-ls
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapFly `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapFly/latest/actions/list-crawled-ur-ls?connectionId=$CONNECTION_ID&limit=25&offset=0&crawlerUuid=bf7282d8-818f-4a17-b3d7-a97a8f49ee65" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "crawlerUuid": "bf7282d8-818f-4a17-b3d7-a97a8f49ee65"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapFly/latest/actions/list-crawled-ur-ls?${params}`, {
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
| `crawlerUuid` | string | yes | Crawler job identifier returned when a crawl starts. Example: `bf7282d8-818f-4a17-b3d7-a97a8f49ee65`. |
| `status` | string | no | Optional crawl URL status filter, such as visited or failed. Example: `visited`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ScrapFly API returns.

## Native endpoint

Through the native ScrapFly API, this operation is `GET /crawl/:crawlerUuid/urls` (base URL `https://api.scrapfly.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-crawled-ur-ls.md) for the provider-specific parameters and requirements.

