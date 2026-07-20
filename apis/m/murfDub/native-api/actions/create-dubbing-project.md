# Create Dubbing Project with Murf Dub

Creates a dubbing project in Murf Dub.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/murfdub/projects/create`
- **Base URL:** `https://api.murf.ai`
- **Official documentation:** [Create Dubbing Project](https://murf.ai/api/docs/api-reference/dubbing/projects/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Project name. |
| `dubbing_type` | body | `string` | yes | Dubbing workflow type. |
| `target_locales[]` | body | `array<string>` | yes | Locales to generate in the project. |
| `source_locale` | body | `string` | no | Source language locale for the project. |
| `description` | body | `string` | no | Project description. |
