# Create Metadata Task with CloudConvert

Creates a metadata task in CloudConvert.

## Endpoint

- **Method:** `POST`
- **Path:** `/metadata`
- **Base URL:** `https://api.cloudconvert.com/v2`
- **Official documentation:** [Create Metadata Task](https://cloudconvert.com/docs/operations/file-metadata)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input[]` | body | `array<string>` | yes | One or more input task IDs to inspect. |
| `input_format` | body | `string` | no | Optional input file format. |
| `engine` | body | `string` | no | Optional metadata engine. |
| `engine_version` | body | `string` | no | Optional metadata engine version. |
| `timeout` | body | `number` | no | Optional timeout in seconds. |
