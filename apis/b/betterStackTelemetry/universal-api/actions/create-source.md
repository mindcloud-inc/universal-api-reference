# Better Stack Telemetry: Create Source

Creates a new telemetry source in Better Stack Telemetry.

```
POST https://connect.mindcloud.co/v1/universal/betterStackTelemetry/latest/actions/create-source
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Better Stack Telemetry `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/betterStackTelemetry/latest/actions/create-source" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "platform": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/betterStackTelemetry/latest/actions/create-source', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "platform": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Source name |
| `platform` | string | yes | Source platform |
| `teamName` | string | no | Required if using a global API token to specify the team that should own the source |
| `sourceGroupId` | number | no | Source group to attach the source to |
| `ingestingPaused` | boolean | no | Whether ingesting is paused for the source |
| `dataRegion` | string | no | Data region or private cluster name to create the source in |
| `liveTailPattern` | string | no | Pattern used for live tail display |
| `logsRetention` | number | no | Data retention for logs in days |
| `metricsRetention` | number | no | Data retention for metrics in days |
| `vrlTransformation` | string | no | VRL transformation to apply to ingested data |
| `scrapeUrls[]` | array<string> | no | URLs to scrape for prometheus_scrape and similar platforms |
| `scrapeFrequencySecs` | number | no | How often to scrape the URLs |
| `scrapeRequestHeaders[]` | array<object> | no | Request headers for scrape requests as an array of objects with name and value |
| `scrapeRequestBasicAuthUser` | string | no | Basic auth username for scrape requests |
| `scrapeRequestBasicAuthPassword` | string | no | Basic auth password for scrape requests |
| `customBucket.name` | string | no | Name of the custom S3-compatible bucket |
| `customBucket.endpoint` | string | no | Endpoint for the custom S3-compatible bucket |
| `customBucket.accessKeyId` | string | no | Access key ID for the custom bucket |
| `customBucket.secretAccessKey` | string | no | Secret access key for the custom bucket |
| `customBucket.keepDataAfterRetention` | boolean | no | Whether to keep data in the bucket after the retention period |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Better Stack Telemetry API returns.

## Native endpoint

Through the native Better Stack Telemetry API, this operation is `POST /api/v1/sources` (base URL `https://telemetry.betterstack.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-source.md) for the provider-specific parameters and requirements.

