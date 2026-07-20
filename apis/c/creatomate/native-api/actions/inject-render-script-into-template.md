# Inject RenderScript Into Template with Creatomate

Creates a render by injecting RenderScript into a template.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/renders`
- **Base URL:** `https://api.creatomate.com`
- **Official documentation:** [Inject RenderScript Into Template](https://creatomate.com/docs/api/quick-start/inject-render-script-into-a-template)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `templateId` | body | `string` | yes | Creatomate template ID to render from. |
| `compositionName` | body | `string` | no | Template composition whose `elements` array should be replaced or appended. |
| `videoUrls[]` | body | `array<string>` | yes | Ordered list of video URLs to inject into the target composition. |
| `appendToExisting` | body | `boolean` | no | Whether to append the videos to the existing composition instead of replacing it. |
