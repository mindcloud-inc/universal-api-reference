# Create Merge Task with CloudConvert

Creates a merge task in CloudConvert.

## Endpoint

- **Method:** `POST`
- **Path:** `/merge`
- **Base URL:** `https://api.cloudconvert.com/v2`
- **Official documentation:** [Create Merge Task](https://cloudconvert.com/docs/operations/merge-files)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input[]` | body | `array<string>` | yes | One or more input task IDs to merge. |
| `output_format` | body | `string` | yes | Target file format. |
| `filename` | body | `string` | no | Optional output filename. |
| `engine` | body | `string` | no | Optional merge engine. |
| `engine_version` | body | `string` | no | Optional merge engine version. |
| `timeout` | body | `number` | no | Optional timeout in seconds. |
