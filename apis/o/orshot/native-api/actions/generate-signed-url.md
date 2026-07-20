# Generate Signed URL with Orshot

## Endpoint

- **Method:** `POST`
- **Path:** `/signed-url/create`
- **Base URL:** `https://api.orshot.com/v1`
- **Official documentation:** [Generate Signed URL](https://orshot.com/docs/api-reference/generate-signed-url)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `modifications.delay` | body | `number` | no | Delay in milliseconds before capture. |
| `modifications.fullCapture` | body | `boolean` | no | Whether to capture the full page when using website screenshot utilities. |
| `modifications.height` | body | `number` | no | Output height for the signed-url render. |
| `modifications.websiteUrl` | body | `string` | no | Public website URL used by utility templates like website-screenshot. |
| `modifications.width` | body | `number` | no | Output width for the signed-url render. |
| `responseFormat` | body | `string` | no | Format for the signed URL render output. |
| `templateId` | body | `string` | yes | Template identifier for generating the signed URL. |
| `renderType` | body | `string` | yes | Render type supported by the template when generating the signed URL. |
| `expiresAt` | body | `number` | no | Optional UNIX timestamp in milliseconds for signed URL expiration. |
