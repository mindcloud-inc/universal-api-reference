# Create Render Job with Renderly

Creates a video render job in Renderly.

## Endpoint

- **Method:** `POST`
- **Path:** `/renders`
- **Base URL:** `https://renderly.video/api/v1`
- **Official documentation:** [Create Render Job](https://renderly.video/api/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `templateId` | body | `string` | no | The template ID to use for template-based rendering. |
| `replacements` | body | `object` | no | Template variable replacements keyed by the template's available variables. |
| `inputProps` | body | `object` | no | Complete direct-render configuration object for advanced non-template rendering. |
| `width` | body | `number` | no | Override video width in pixels. |
| `height` | body | `number` | no | Override video height in pixels. |
| `fps` | body | `number` | no | Override frames per second. |
| `durationInFrames` | body | `number` | no | Override total video duration in frames. |
| `createProject` | body | `boolean` | no | Whether to create a project for this render job. |
| `projectName` | body | `string` | no | Name for the created project when Create Project is enabled. |
| `webhookUrl` | body | `string` | no | One-off webhook URL to notify when the render completes or fails. |
