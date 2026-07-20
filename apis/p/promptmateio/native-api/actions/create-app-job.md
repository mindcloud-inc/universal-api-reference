# Create App Job with Promptmate.io

## Endpoint

- **Method:** `POST`
- **Path:** `/app-jobs`
- **Base URL:** `https://api.promptmate.io/v1`
- **Official documentation:** [Create App Job](https://apidoc.promptmate.io/api-4935445)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | body | `string` | yes | The Promptmate app ID to run. |
| `callBackUrl` | body | `string` | no | Optional callback URL for job completion notifications. |
| `noMailOnFinish` | body | `boolean` | no | Disable Promptmate completion emails for the job. |
| `data[]` | body | `array<object>` | yes | Array of input objects. Promptmate expects an array of single-key objects matching the app data-field labels, for example [{"Image URL":"https://example.com/test.png"}]. |
