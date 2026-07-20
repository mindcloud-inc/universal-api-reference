# List Presets with Rebrandly

Retrieves presets for a template in Rebrandly.

## Endpoint

- **Method:** `GET`
- **Path:** `https://templating.rebrandly.com/v1/url/querystring/templates/:templateId/presets`
- **Base URL:** `https://api.rebrandly.com/v1`
- **Official documentation:** [List Presets](https://developers.rebrandly.com/docs/getting-presets-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `templateId` | path | `string` | yes | Template identifier returned by List Templates. |
