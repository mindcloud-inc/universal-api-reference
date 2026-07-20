# Update Preset with Auphonic

Updates an existing preset in Auphonic.

## Endpoint

- **Method:** `POST`
- **Path:** `/preset/:uuid.json`
- **Base URL:** `https://auphonic.com/api`
- **Official documentation:** [Update Preset](https://auphonic.com/help/api/update.html#update-a-production-or-preset-and-reset-data)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uuid` | path | `string` | yes | UUID of the preset. |
| `preset_name` | body | `string` | yes | Updated preset name. |
