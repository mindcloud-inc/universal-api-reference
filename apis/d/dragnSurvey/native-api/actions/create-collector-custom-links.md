# Create Collector Custom Links with Drag'n Survey

Creates respondent identification links for a Drag'n Survey collector.

## Endpoint

- **Method:** `POST`
- **Path:** `collectors/:collectorId/authenticate`
- **Base URL:** `https://developer.dragnsurvey.com/api/v2.0.0`
- **Official documentation:** [Create Collector Custom Links](https://developer.dragnsurvey.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collectorId` | path | `string` | no | The Drag'n Survey collector ID. |
| `respondents_informations` | body | `string` | no | Array of objects to embed into generated authenticated collector links. |
