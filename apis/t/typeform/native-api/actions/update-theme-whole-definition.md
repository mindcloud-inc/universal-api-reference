# Update Theme (Whole Definition) with Typeform

## Endpoint

- **Method:** `PUT`
- **Path:** `/themes/:themeId`
- **Base URL:** `https://api.typeform.com`
- **Official documentation:** [Update Theme (Whole Definition)](https://www.typeform.com/developers/create/reference/update-theme-whole-definition/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `background` | body | `string` | no | Theme background settings. |
| `colors` | body | `boolean` | no | Theme colors configuration. |
| `fields` | body | `string` | no | Theme field styles. |
| `font` | body | `string` | no | Theme font settings. |
| `has_transparent_button` | body | `string` | no | Whether buttons are transparent. |
| `name` | body | `string` | no | Theme name. |
| `rounded_corners` | body | `string` | no | Corner radius settings. |
| `screens` | body | `string` | no | Screen theme settings. |
| `themeId` | path | `string` | yes | Typeform theme identifier. |
