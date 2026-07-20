# GrowthBook: Create a single fact metric

Creates a new fact metric in GrowthBook.

```
POST https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/post-fact-metric
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GrowthBook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/post-fact-metric" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "sample",
  "metricType": "sample",
  "numerator": {
    "sample": "value"
  }
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/post-fact-metric', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "sample",
    "metricType": "sample",
    "numerator": {"sample":"value"}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Default: `sample`. |
| `description` | string | no |  |
| `owner` | string | no | The userId or email address of the owner. If an email address is provided, it will be used to look up the userId of the matching organization member. If an ID is provided, it will be validated as existing in the organization. |
| `projects` | list<string> | no |  |
| `tags` | list<string> | no |  |
| `metricType` | string | yes | Default: `sample`. |
| `numerator` | object | yes | Default: `{"sample":"value"}`. |
| `denominator` | object | no | Only when metricType is 'ratio' |
| `inverse` | boolean | no | Set to true for things like Bounce Rate, where you want the metric to decrease |
| `quantileSettings` | object | no | Controls the settings for quantile metrics (mandatory if metricType is "quantile") |
| `cappingSettings` | object | no | Controls how outliers are handled |
| `windowSettings` | object | no | Controls the conversion window for the metric |
| `priorSettings` | object | no | Controls the bayesian prior for the metric. If omitted, organization defaults will be used. |
| `regressionAdjustmentSettings` | object | no | Controls the regression adjustment (CUPED) settings for the metric |
| `riskThresholdSuccess` | number | no | No longer used. Threshold for Risk to be considered low enough, as a proportion (e.g. put 0.0025 for 0.25%). <br/> Must be a non-negative number and must not be higher than `riskThresholdDanger`. |
| `riskThresholdDanger` | number | no | No longer used. Threshold for Risk to be considered too high, as a proportion (e.g. put 0.0125 for 1.25%). <br/> Must be a non-negative number. |
| `displayAsPercentage` | boolean | no | If true and the metric is a ratio or dailyParticipation metric, variation means will be displayed as a percentage. Defaults to true for dailyParticipation metrics and false for ratio metrics. |
| `minPercentChange` | number | no | Minimum percent change to consider uplift significant, as a proportion (e.g. put 0.005 for 0.5%) |
| `maxPercentChange` | number | no | Maximum percent change to consider uplift significant, as a proportion (e.g. put 0.5 for 50%) |
| `minSampleSize` | number | no |  |
| `targetMDE` | number | no | The percentage change that you want to reliably detect before ending an experiment, as a proportion (e.g. put 0.1 for 10%). This is used to estimate the "Days Left" for running experiments. |
| `managedBy` | string | no | Set this to "api" to disable editing in the GrowthBook UI |
| `metricAutoSlices` | list<string> | no | Array of slice column names that will be automatically included in metric analysis. This is an enterprise feature. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "factMetric": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `factMetric` | object |  |

## Native endpoint

Through the native GrowthBook API, this operation is `POST /fact-metrics` (base URL `https://api.growthbook.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/post-fact-metric.md) for the provider-specific parameters and requirements.

