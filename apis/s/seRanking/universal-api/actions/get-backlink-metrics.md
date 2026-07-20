# SE Ranking Data: Get backlink metrics

Retrieves backlink metrics from SE Ranking Data.

```
GET https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-backlink-metrics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SE Ranking Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-backlink-metrics?connectionId=$CONNECTION_ID&target=seranking.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "target": "seranking.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-backlink-metrics?${params}`, {
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
| `target` | string | yes | Target domain or URL to analyze (for example: seranking.com). Example: `seranking.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "metrics": [
        {
          "backlinks": 1,
          "dofollowBacklinks": 1,
          "eduBacklinks": 1,
          "govBacklinks": 1,
          "ips": 1,
          "nofollowBacklinks": 1,
          "refdomains": 1,
          "subnets": 1,
          "target": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `metrics` | array<object> | Backlink metrics rows. |
| `metrics[].backlinks` | number |  |
| `metrics[].dofollowBacklinks` | number |  |
| `metrics[].eduBacklinks` | number |  |
| `metrics[].govBacklinks` | number |  |
| `metrics[].ips` | number |  |
| `metrics[].nofollowBacklinks` | number |  |
| `metrics[].refdomains` | number |  |
| `metrics[].subnets` | number |  |
| `metrics[].target` | string |  |

## Native endpoint

Through the native SE Ranking Data API, this operation is `GET /backlinks/metrics` (base URL `https://api.seranking.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-backlink-metrics.md) for the provider-specific parameters and requirements.

