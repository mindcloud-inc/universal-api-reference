# Better Stack Telemetry: Update Source

Updates an existing telemetry source in Better Stack Telemetry.

```
PUT https://connect.mindcloud.co/v1/universal/betterStackTelemetry/latest/actions/update-source
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Better Stack Telemetry `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/betterStackTelemetry/latest/actions/update-source" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sourceId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/betterStackTelemetry/latest/actions/update-source', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sourceId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sourceId` | string | yes | ID of the source to update |
| `name` | string | no | Source name |
| `ingestingPaused` | boolean | no | Whether ingesting is paused for the source |
| `sourceGroupId` | number | no | Source group to attach the source to |
| `liveTailPattern` | string | no | Pattern used for live tail display |
| `logsRetention` | number | no | Data retention for logs in days |
| `metricsRetention` | number | no | Data retention for metrics in days |
| `vrlTransformation` | string | no | VRL transformation to apply to ingested data |
| `scrapeUrls[]` | array<string> | no | URLs to scrape for prometheus_scrape and similar platforms |
| `scrapeFrequencySecs` | number | no | How often to scrape the URLs |
| `scrapeRequestHeaders[]` | array<object> | no | Request headers for scrape requests as an array of objects with name and value |
| `scrapeRequestBasicAuthUser` | string | no | Basic auth username for scrape requests |
| `scrapeRequestBasicAuthPassword` | string | no | Basic auth password for scrape requests |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Better Stack Telemetry API returns.

## Native endpoint

Through the native Better Stack Telemetry API, this operation is `PATCH /api/v1/sources/:source_id` (base URL `https://telemetry.betterstack.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-source.md) for the provider-specific parameters and requirements.

