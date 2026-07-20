# List Presets with Auphonic

Retrieves presets from Auphonic.

## Endpoint

- **Method:** `GET`
- **Path:** `/presets.json`
- **Base URL:** `https://auphonic.com/api`
- **Official documentation:** [List Presets](https://auphonic.com/help/api/query.html#list-all-productions-and-presets)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `preset_type` | query | `list<string>` | no | Choose which preset set to return. Accepted values: `all_presets`, `auphonic_presets`, `personal_presets`. |
| `minimal_data` | query | `boolean` | no | Return only minimal preset data. |
| `uuids_only` | query | `boolean` | no | Return only preset UUIDs. |
