# Create Archive Task with CloudConvert

Creates an archive task in CloudConvert.

## Endpoint

- **Method:** `POST`
- **Path:** `/archive`
- **Base URL:** `https://api.cloudconvert.com/v2`
- **Official documentation:** [Create Archive Task](https://cloudconvert.com/docs/operations/create-archives)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input[]` | body | `array<string>` | yes | One or more input task IDs to archive. |
| `output_format` | body | `string` | yes | Target archive file format. |
| `filename` | body | `string` | no | Optional archive filename. |
| `engine` | body | `string` | no | Optional archive engine. |
| `engine_version` | body | `string` | no | Optional archive engine version. |
| `timeout` | body | `number` | no | Optional timeout in seconds. |
