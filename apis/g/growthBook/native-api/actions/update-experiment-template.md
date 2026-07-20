# Update a single experimentTemplate with GrowthBook

Updates an existing experiment template in GrowthBook.

## Endpoint

- **Method:** `PUT`
- **Path:** `/experiment-templates/:id`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Update a single experimentTemplate](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `project` | body | `string` | no |
| `templateMetadata` | body | `object` | no |
| `type` | body | `string` | no |
| `hypothesis` | body | `string` | no |
| `description` | body | `string` | no |
| `tags` | body | `list<string>` | no |
| `customFields` | body | `object` | no |
| `datasource` | body | `string` | no |
| `exposureQueryId` | body | `string` | no |
| `hashAttribute` | body | `string` | no |
| `fallbackAttribute` | body | `string` | no |
| `disableStickyBucketing` | body | `boolean` | no |
| `goalMetrics` | body | `list<string>` | no |
| `secondaryMetrics` | body | `list<string>` | no |
| `guardrailMetrics` | body | `list<string>` | no |
| `activationMetric` | body | `string` | no |
| `statsEngine` | body | `string` | no |
| `segment` | body | `string` | no |
| `skipPartialData` | body | `boolean` | no |
| `targeting` | body | `object` | no |
| `customMetricSlices[]` | body | `array<object>` | no |
