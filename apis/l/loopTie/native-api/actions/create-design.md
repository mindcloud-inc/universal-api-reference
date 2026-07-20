# Create Design with Loop & Tie

Creates a new design in Loop & Tie.

## Endpoint

- **Method:** `POST`
- **Path:** `/teams/:teamId/designs`
- **Base URL:** `https://api.loopandtie.com/v1`
- **Official documentation:** [Create Design](https://docs.loopandtie.com/reference/teamsteam_iddesigns-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `design[image_url]` | query | `string` | no | Public image URL for the design hero image. |
| `design[name]` | query | `string` | no | Display name for the design. |
| `teamId` | path | `string` | no | The Loop & Tie team ID. |
