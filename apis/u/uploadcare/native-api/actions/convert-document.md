# Convert Document with Uploadcare

Creates a document conversion in Uploadcare.

## Endpoint

- **Method:** `POST`
- **Path:** `/convert/document/`
- **Base URL:** `https://api.uploadcare.com`
- **Official documentation:** [Convert Document](https://uploadcare.com/api-refs/rest-api/v0.7.0/#tag/Conversion/operation/documentConvert)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `paths[]` | body | `array<string>` | yes | List of source file paths to convert. |
| `save_in_group` | body | `string` | no | Whether to save multi-page conversion output into a group. |
| `store` | body | `string` | no | Whether to store converted files permanently. |
