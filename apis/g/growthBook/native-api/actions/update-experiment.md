# Update a single experiment with GrowthBook

Updates an existing experiment in GrowthBook.

## Endpoint

- **Method:** `POST`
- **Path:** `/experiments/:id`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Update a single experiment](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The id of the requested resource |
| `datasourceId` | body | `string` | no | Can only be set if existing experiment does not have a datasource |
| `assignmentQueryId` | body | `string` | no | — |
| `trackingKey` | body | `string` | no | — |
| `bypassDuplicateKeyCheck` | body | `boolean` | no | If true, allow updating the tracking key even if another experiment with the same tracking key already exists |
| `name` | body | `string` | no | Name of the experiment |
| `type` | body | `string` | no | — |
| `project` | body | `string` | no | Project ID which the experiment belongs to |
| `hypothesis` | body | `string` | no | Hypothesis of the experiment |
| `description` | body | `string` | no | Description of the experiment |
| `tags` | body | `list<string>` | no | — |
| `metrics` | body | `list<string>` | no | — |
| `secondaryMetrics` | body | `list<string>` | no | — |
| `guardrailMetrics` | body | `list<string>` | no | — |
| `activationMetric` | body | `string` | no | Users must convert on this metric before being included |
| `segmentId` | body | `string` | no | Only users in this segment will be included |
| `queryFilter` | body | `string` | no | WHERE clause to add to the default experiment query |
| `owner` | body | `string` | no | The userId or email address of the owner. If an email address is provided, it will be used to look up the userId of the matching organization member. If an ID is provided, it will be validated as existing in the organization. |
| `archived` | body | `boolean` | no | — |
| `status` | body | `string` | no | — |
| `autoRefresh` | body | `boolean` | no | — |
| `hashAttribute` | body | `string` | no | — |
| `fallbackAttribute` | body | `string` | no | — |
| `hashVersion` | body | `number` | no | — |
| `disableStickyBucketing` | body | `boolean` | no | — |
| `bucketVersion` | body | `number` | no | — |
| `minBucketVersion` | body | `number` | no | — |
| `results` | body | `string` | no | The result status of the experiment. Maps to resultSummary.status in the GET response. |
| `winner` | body | `number` | no | The index of the winning variation (0-indexed). Maps to resultSummary.winner (variation ID) in the GET response. |
| `analysis` | body | `string` | no | Analysis summary or conclusions for the experiment. Maps to resultSummary.conclusions in the GET response. |
| `releasedVariationId` | body | `string` | no | The ID of the released variation. Maps to resultSummary.releasedVariationId in the GET response. |
| `excludeFromPayload` | body | `boolean` | no | If true, the experiment is excluded from the SDK payload. Maps to resultSummary.excludeFromPayload in the GET response. |
| `inProgressConversions` | body | `string` | no | — |
| `attributionModel` | body | `string` | no | Setting attribution model to `"experimentDuration"` is the same as selecting "Ignore Conversion Windows" for the Conversion Window Override. Setting it to `"lookbackOverride"` requires a `lookbackOverride` object to be provided. |
| `lookbackOverride` | body | `object` | no | Controls the lookback override for the experiment. For type "window", value must be a non-negative number and valueUnit is required. |
| `statsEngine` | body | `string` | no | — |
| `variations[]` | body | `array<object>` | no | — |
| `variations[]` | body | `array<object>` | no | — |
| `phases[]` | body | `array<object>` | no | — |
| `phases[]` | body | `array<object>` | no | — |
| `regressionAdjustmentEnabled` | body | `boolean` | no | Controls whether regression adjustment (CUPED) is enabled for experiment analyses |
| `sequentialTestingEnabled` | body | `boolean` | no | Only applicable to frequentist analyses |
| `sequentialTestingTuningParameter` | body | `number` | no | — |
| `shareLevel` | body | `string` | no | — |
| `banditScheduleValue` | body | `number` | no | — |
| `banditScheduleUnit` | body | `string` | no | — |
| `banditBurnInValue` | body | `number` | no | — |
| `banditBurnInUnit` | body | `string` | no | — |
| `banditConversionWindowValue` | body | `number` | no | — |
| `banditConversionWindowUnit` | body | `string` | no | — |
| `postStratificationEnabled` | body | `boolean` | no | When null, the organization default is used. |
| `decisionFrameworkSettings` | body | `object` | no | Controls the decision framework and metric overrides for the experiment. Replaces the entire stored object on update (does not patch individual fields). |
| `metricOverrides[]` | body | `array<object>` | no | Per-metric analysis overrides for this experiment. Replaces the entire stored array (does not patch individual entries). |
| `metricOverrides[]` | body | `array<object>` | no | Per-metric analysis overrides for this experiment. Replaces the entire stored array (does not patch individual entries). |
| `defaultDashboardId` | body | `string` | no | ID of the default dashboard for this experiment. |
| `customFields` | body | `object` | no | — |
| `customMetricSlices[]` | body | `array<object>` | no | Custom slices that apply to ALL applicable metrics in the experiment |
| `customMetricSlices[]` | body | `array<object>` | no | Custom slices that apply to ALL applicable metrics in the experiment |
