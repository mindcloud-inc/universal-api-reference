# Concatenate Multiple Videos with Creatomate

Creates a concatenated video render in Creatomate.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/renders`
- **Base URL:** `https://api.creatomate.com`
- **Official documentation:** [Concatenate Multiple Videos](https://creatomate.com/docs/api/quick-start/concatenate-multiple-videos)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `videoUrls[]` | body | `array<string>` | yes | Ordered list of video URLs to concatenate into one render. |
| `includeFadeTransition` | body | `boolean` | no | Whether to add the documented fade transition between clips after the first. |
| `transitionDurationSeconds` | body | `number` | no | Duration of the transition animation in seconds. |
| `transitionType` | body | `string` | no | Creatomate transition type to apply between video clips. |
