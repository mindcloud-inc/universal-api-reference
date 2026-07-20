# Upload Logo with Loop & Tie

Creates a new logo in Loop & Tie.

## Endpoint

- **Method:** `POST`
- **Path:** `/teams/:teamId/logos`
- **Base URL:** `https://api.loopandtie.com/v1`
- **Official documentation:** [Upload Logo](https://docs.loopandtie.com/reference/teamsteam_idlogos-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `logo[image_url]` | query | `string` | no | Public image URL for the logo. |
| `logo[name]` | query | `string` | no | Display name for the logo. |
| `teamId` | path | `string` | no | The Loop & Tie team ID. |
