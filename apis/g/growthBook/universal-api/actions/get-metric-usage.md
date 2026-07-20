# GrowthBook: Get metric usage across experiments

Retrieves metric usage across GrowthBook experiments.

```
GET https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/get-metric-usage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GrowthBook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/get-metric-usage?connectionId=$CONNECTION_ID&ids=sample" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ids": "sample"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/get-metric-usage?${params}`, {
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
| `ids` | string | yes | List of comma-separated metric IDs (both fact and legacy) to get usage for, e.g. ids=met_123,fact_456 Default: `sample`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "metricUsage": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `metricUsage` | array<object> |  |

## Native endpoint

Through the native GrowthBook API, this operation is `GET /usage/metrics` (base URL `https://api.growthbook.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-metric-usage.md) for the provider-specific parameters and requirements.

