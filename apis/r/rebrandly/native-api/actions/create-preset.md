# Create Preset with Rebrandly

Creates a preset for a template in Rebrandly.

## Endpoint

- **Method:** `POST`
- **Path:** `https://templating.rebrandly.com/v1/url/querystring/templates/:templateId/presets`
- **Base URL:** `https://api.rebrandly.com/v1`
- **Official documentation:** [Create Preset](https://developers.rebrandly.com/docs/creating-a-preset-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `templateId` | path | `string` | yes | Template identifier returned by List Templates. |
| `name` | body | `string` | yes | Human-friendly preset name. |
