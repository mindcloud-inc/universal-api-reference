# Deep Infra: Get Deployment Stats



```
GET https://connect.mindcloud.co/v1/universal/deepInfra/latest/actions/get-deployment-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deep Infra `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deepInfra/latest/actions/get-deployment-stats?connectionId=$CONNECTION_ID&deployId=string&from=2026-04-22T20%3A00%3A00Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "deployId": "string",
  "from": "2026-04-22T20:00:00Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deepInfra/latest/actions/get-deployment-stats?${params}`, {
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
| `deployId` | string | yes | Dedicated deployment identifier from the deployment stats URL path. |
| `from` | string | yes | Start of stats period as a Unix timestamp or relative value such as now-1h. Example: `2026-04-22T20:00:00Z`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deploy_id": "string",
      "errors": 1,
      "from": "string",
      "latency_ms": 1,
      "requests": 1,
      "to": "string",
      "tokens": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deploy_id` | string | Deployment identifier. |
| `errors` | number | Error count during the stats window. |
| `from` | string | Stats start time. |
| `latency_ms` | number | Latency in milliseconds when returned. |
| `requests` | number | Request count during the stats window. |
| `to` | string | Stats end time when returned. |
| `tokens` | number | Token count during the stats window. |

## Native endpoint

Through the native Deep Infra API, this operation is `GET /deploy/:deploy_id/stats` (base URL `https://api.deepinfra.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-deployment-stats.md) for the provider-specific parameters and requirements.

