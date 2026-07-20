# Postcopytransform with GrowthBook

Copies a transform in your GrowthBook organization.

## Endpoint

- **Method:** `POST`
- **Path:** `/transform-copy`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Postcopytransform](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `visualChangesetId` | body | `string` | yes |
| `copy` | body | `string` | yes |
| `mode` | body | `string` | yes |
