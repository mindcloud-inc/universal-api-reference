# Control A Character with Runway

Creates a character performance task in Runway.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/character_performance`
- **Base URL:** `https://api.dev.runwayml.com`
- **Official documentation:** [Control A Character](https://docs.dev.runwayml.com/api#tag/Start-generating/paths/~1v1~1character_performance/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `character` | body | `object` | yes | Character object with type and uri for the image or video character source. |
| `model` | body | `string` | yes | Runway currently requires act_two. |
| `reference` | body | `object` | yes | Reference video object containing the performance to apply. |
