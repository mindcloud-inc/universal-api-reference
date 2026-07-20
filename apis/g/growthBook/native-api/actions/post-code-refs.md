# Submit list of code references with GrowthBook

Submits code references to your GrowthBook organization.

## Endpoint

- **Method:** `POST`
- **Path:** `/code-refs`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Submit list of code references](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `deleteMissing` | query | `string` | no | Whether to delete code references that are no longer present in the submitted data |
| `branch` | body | `string` | yes | — |
| `repoName` | body | `string` | yes | — |
| `refs[]` | body | `array<object>` | yes | — |
