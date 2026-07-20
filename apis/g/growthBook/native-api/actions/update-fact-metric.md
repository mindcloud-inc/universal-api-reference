# Update a single fact metric with GrowthBook

Updates an existing fact metric in GrowthBook.

## Endpoint

- **Method:** `POST`
- **Path:** `/fact-metrics/:id`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Update a single fact metric](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The id of the requested resource |
| `name` | body | `string` | no | — |
| `description` | body | `string` | no | — |
| `owner` | body | `string` | no | The userId or email address of the owner. If an email address is provided, it will be used to look up the userId of the matching organization member. If an ID is provided, it will be validated as existing in the organization. |
| `projects` | body | `list<string>` | no | — |
| `tags` | body | `list<string>` | no | — |
| `metricType` | body | `string` | no | — |
| `numerator` | body | `object` | no | — |
| `denominator` | body | `object` | no | Only when metricType is 'ratio' |
| `inverse` | body | `boolean` | no | Set to true for things like Bounce Rate, where you want the metric to decrease |
| `quantileSettings` | body | `object` | no | Controls the settings for quantile metrics (mandatory if metricType is "quantile") |
| `cappingSettings` | body | `object` | no | Controls how outliers are handled |
| `windowSettings` | body | `object` | no | Controls the conversion window for the metric |
| `priorSettings` | body | `object` | no | Controls the bayesian prior for the metric. If omitted, organization defaults will be used. |
| `regressionAdjustmentSettings` | body | `object` | no | Controls the regression adjustment (CUPED) settings for the metric |
| `riskThresholdSuccess` | body | `number` | no | No longer used. Threshold for Risk to be considered low enough, as a proportion (e.g. put 0.0025 for 0.25%). <br/> Must be a non-negative number and must not be higher than `riskThresholdDanger`. |
| `riskThresholdDanger` | body | `number` | no | No longer used. Threshold for Risk to be considered too high, as a proportion (e.g. put 0.0125 for 1.25%). <br/> Must be a non-negative number. |
| `displayAsPercentage` | body | `boolean` | no | If true and the metric is a ratio or dailyParticipation metric, variation means will be displayed as a percentage. Defaults to true for dailyParticipation metrics and false for ratio metrics. |
| `minPercentChange` | body | `number` | no | Minimum percent change to consider uplift significant, as a proportion (e.g. put 0.005 for 0.5%) |
| `maxPercentChange` | body | `number` | no | Maximum percent change to consider uplift significant, as a proportion (e.g. put 0.5 for 50%) |
| `minSampleSize` | body | `number` | no | — |
| `targetMDE` | body | `number` | no | — |
| `managedBy` | body | `string` | no | Set this to "api" to disable editing in the GrowthBook UI |
| `archived` | body | `boolean` | no | — |
| `metricAutoSlices` | body | `list<string>` | no | Array of slice column names that will be automatically included in metric analysis. This is an enterprise feature. |
