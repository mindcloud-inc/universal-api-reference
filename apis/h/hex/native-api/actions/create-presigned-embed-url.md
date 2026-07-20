# Create Presigned Embed URL with Hex

## Endpoint

- **Method:** `POST`
- **Path:** `/embedding/createPresignedUrl/{projectId}`
- **Base URL:** `https://app.hex.tech/api/v1`
- **Official documentation:** [Create Presigned Embed URL](https://learn.hex.tech/docs/api-integrations/api/reference#operation/CreatePresignedUrl)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `displayOptions.theme` | body | `string` | no | — |
| `expiresIn` | body | `number` | no | — |
| `projectId` | path | `string` | yes | Unique ID for a Hex project. |
| `scope[]` | body | `array<string>` | no | — |
| `testMode` | body | `boolean` | no | — |
