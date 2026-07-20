# ScrapeOps: Run Spider

Runs a spider on a ScrapeOps server.

```
POST https://connect.mindcloud.co/v1/universal/scrapeOps/latest/actions/run-spider
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapeOps `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/scrapeOps/latest/actions/run-spider" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "serverId": 1,
  "selectedSpiderId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/scrapeOps/latest/actions/run-spider', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "serverId": 1,
    "selectedSpiderId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `serverId` | number | yes | The numeric ScrapeOps server id that owns the spider. |
| `selectedSpiderId` | number | yes | The numeric spider id to run on the selected server. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ScrapeOps API returns.

## Native endpoint

Through the native ScrapeOps API, this operation is `POST https://backend.scrapeops.io/v1/client/spiders/run` (base URL `http://headers.scrapeops.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/run-spider.md) for the provider-specific parameters and requirements.

