# Get Template with Print.one Postcards

Retrieves a template from Print.one Postcards.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/templates/[:id]/[:version]`
- **Base URL:** `https://api.print.one`
- **Official documentation:** [Get Template](https://api.print.one/docs/v2#operation/Template/getTemplate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Template ID. |
| `version` | path | `number` | yes | Template version. |
