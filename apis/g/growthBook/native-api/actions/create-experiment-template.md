# Create a single experimentTemplate with GrowthBook

Creates a new experiment template in GrowthBook.

## Endpoint

- **Method:** `POST`
- **Path:** `/experiment-templates`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Create a single experimentTemplate](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `project` | body | `string` | no |
| `templateMetadata` | body | `object` | yes |
| `type` | body | `string` | yes |
| `hypothesis` | body | `string` | no |
| `description` | body | `string` | no |
| `tags` | body | `list<string>` | no |
| `customFields` | body | `object` | no |
| `datasource` | body | `string` | yes |
| `exposureQueryId` | body | `string` | yes |
| `hashAttribute` | body | `string` | no |
| `fallbackAttribute` | body | `string` | no |
| `disableStickyBucketing` | body | `boolean` | no |
| `goalMetrics` | body | `list<string>` | no |
| `secondaryMetrics` | body | `list<string>` | no |
| `guardrailMetrics` | body | `list<string>` | no |
| `activationMetric` | body | `string` | no |
| `statsEngine` | body | `string` | yes |
| `segment` | body | `string` | no |
| `skipPartialData` | body | `boolean` | no |
| `targeting` | body | `object` | yes |
| `customMetricSlices[]` | body | `array<object>` | no |
