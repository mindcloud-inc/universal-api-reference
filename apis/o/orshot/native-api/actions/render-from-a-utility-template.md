# Render from a Utility Template with Orshot

## Endpoint

- **Method:** `POST`
- **Path:** `/generate/:renderType`
- **Base URL:** `https://api.orshot.com/v1`
- **Official documentation:** [Render from a Utility Template](https://orshot.com/docs/api-reference/render-from-template)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `modifications.delay` | body | `number` | no | Delay in milliseconds before capture. |
| `modifications.fullCapture` | body | `boolean` | no | Whether to capture the full page when using website screenshot utilities. |
| `modifications.height` | body | `number` | no | Output height for the utility render. |
| `modifications.websiteUrl` | body | `string` | no | Public website URL used by utility templates like website-screenshot. |
| `modifications.width` | body | `number` | no | Output width for the utility render. |
| `renderType` | path | `string` | yes | Utility template render type such as images or pdfs. |
| `response.format` | body | `string` | no | Format for the generated output. |
| `response.type` | body | `string` | no | Return type for the generated output. |
| `templateId` | body | `string` | yes | Utility template identifier. |
