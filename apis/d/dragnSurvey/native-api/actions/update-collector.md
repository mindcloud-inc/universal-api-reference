# Update Collector with Drag'n Survey

Updates a collector in Drag'n Survey.

## Endpoint

- **Method:** `PATCH`
- **Path:** `collectors/:collectorId`
- **Base URL:** `https://developer.dragnsurvey.com/api/v2.0.0`
- **Official documentation:** [Update Collector](https://developer.dragnsurvey.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collectorId` | path | `string` | no | The Drag'n Survey collector ID. |
| `status` | body | `string` | no | Collector status. |
| `title` | body | `string` | no | Updated collector title. |
