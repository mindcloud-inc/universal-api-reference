# Upsert Preset with Typesense

Creates or updates a search preset in Typesense.

## Endpoint

- **Method:** `PUT`
- **Path:** `/presets/{{presetName}}`
- **Base URL:** `https://5brh8vz1lictf0jop-1.a2.typesense.net`
- **Official documentation:** [Upsert Preset](https://typesense.org/docs/30.0/api/search.html#presets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `preset` | body | `object` | yes | Preset definition JSON body. |
| `presetName` | path | `string` | yes | Preset name. |
