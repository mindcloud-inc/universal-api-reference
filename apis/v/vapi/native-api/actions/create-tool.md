# Create Tool with Vapi

Creates a new tool in Vapi.

## Endpoint

- **Method:** `POST`
- **Path:** `/tool`
- **Base URL:** `https://api.vapi.ai`
- **Official documentation:** [Create Tool](https://docs.vapi.ai/api-reference/tools/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | body | `string` | yes | Discriminator value: apiRequest |
| `messages[]` | body | `array<object>` | no | These are the messages that will be spoken to the user as the tool is running.  For some tools, this is auto-filled based on special fields like `tool.destinations`. For others like the function tool, these can be custom configured. |
| `method` | body | `string` | yes | — |
| `timeoutSeconds` | body | `number` | no | This is the timeout in seconds for the request. Defaults to 20 seconds.  @default 20 |
| `credentialId` | body | `string` | no | The credential ID for API request authentication |
| `encryptedPaths[]` | body | `array<string>` | no | This is the paths to encrypt in the request body if credentialId and encryptionPlan are defined. |
| `name` | body | `string` | no | This is the name of the tool. This will be passed to the model.  Must be a-z, A-Z, 0-9, or contain underscores and dashes, with a maximum length of 40. |
| `description` | body | `string` | no | This is the description of the tool. This will be passed to the model. |
| `url` | body | `string` | yes | This is where the request will be sent. |
| `body` | body | `object` | no | — |
| `headers` | body | `object` | no | — |
| `backoffPlan` | body | `object` | no | — |
| `variableExtractionPlan` | body | `object` | no | — |
| `rejectionPlan` | body | `object` | no | — |
| `parameters[]` | body | `array<object>` | no | Static key-value pairs merged into the request body or function arguments. Values support Liquid templates. |
