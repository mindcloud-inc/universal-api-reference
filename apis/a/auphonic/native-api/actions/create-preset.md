# Create Preset with Auphonic

Creates a new preset in Auphonic.

## Endpoint

- **Method:** `POST`
- **Path:** `/presets.json`
- **Base URL:** `https://auphonic.com/api`
- **Official documentation:** [Create Preset](https://auphonic.com/help/api/details.html#creation-of-presets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `preset_name` | body | `string` | yes | Name for the new preset. |
| `is_multitrack` | body | `boolean` | no | Create the preset as multitrack. |
