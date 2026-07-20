# Populate Preset with Rebrandly

Populates a preset for a template in Rebrandly.

## Endpoint

- **Method:** `POST`
- **Path:** `https://templating.rebrandly.com/v1/url/querystring/templates/:templateId/presets/:presetId`
- **Base URL:** `https://api.rebrandly.com/v1`
- **Official documentation:** [Populate Preset](https://developers.rebrandly.com/docs/updating-a-preset)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `templateId` | path | `string` | yes | Template identifier returned by List Templates. |
| `presetId` | path | `string` | yes | Preset identifier returned by Create Preset or List Presets. |
| `name` | body | `string` | yes | Human-friendly preset name. |
| `data` | body | `object` | yes | Preset data object containing a query object keyed by parameter ID. |
