# ScrapFly: Cancel Crawl

Cancels an existing crawl job in ScrapFly.

```
DELETE https://connect.mindcloud.co/v1/universal/scrapFly/latest/actions/cancel-crawl
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapFly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/scrapFly/latest/actions/cancel-crawl?connectionId=$CONNECTION_ID&crawlerUuid=bf7282d8-818f-4a17-b3d7-a97a8f49ee65" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "crawlerUuid": "bf7282d8-818f-4a17-b3d7-a97a8f49ee65"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapFly/latest/actions/cancel-crawl?${params}`, {
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

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ScrapFly API returns.

## Native endpoint

Through the native ScrapFly API, this operation is `DELETE /crawl/:crawlerUuid` (base URL `https://api.scrapfly.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-crawl.md) for the provider-specific parameters and requirements.

