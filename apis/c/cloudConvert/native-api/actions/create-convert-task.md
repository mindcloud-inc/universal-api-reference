# Create Convert Task with CloudConvert

Creates a convert task in CloudConvert.

## Endpoint

- **Method:** `POST`
- **Path:** `/convert`
- **Base URL:** `https://api.cloudconvert.com/v2`
- **Official documentation:** [Create Convert Task](https://cloudconvert.com/docs/operations/convert-files)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input[]` | body | `array<string>` | yes | One or more input task IDs to convert. |
| `output_format` | body | `string` | yes | Target file format. |
| `input_format` | body | `string` | no | Optional input file format. |
| `filename` | body | `string` | no | Optional output filename. |
| `engine` | body | `string` | no | Optional conversion engine. |
| `engine_version` | body | `string` | no | Optional conversion engine version. |
| `timeout` | body | `number` | no | Optional timeout in seconds. |
