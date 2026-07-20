# Delete Preset with Rebrandly

Deletes a preset from a template in Rebrandly.

## Endpoint

- **Method:** `DELETE`
- **Path:** `https://templating.rebrandly.com/v1/url/querystring/templates/:templateId/presets/:presetId`
- **Base URL:** `https://api.rebrandly.com/v1`
- **Official documentation:** [Delete Preset](https://developers.rebrandly.com/docs/delete-a-preset)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `templateId` | path | `string` | yes | Template identifier returned by List Templates. |
| `presetId` | path | `string` | yes | Preset identifier returned by Create Preset or List Presets. |
