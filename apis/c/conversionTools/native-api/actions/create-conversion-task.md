# Create Conversion Task with Conversion Tools

Creates a new conversion task in Conversion Tools.

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks`
- **Base URL:** `https://api.conversiontools.io/v1`
- **Official documentation:** [Create Conversion Task](https://conversiontools.io/api-documentation#run-conversion-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | body | `string` | yes | Conversion type identifier from Conversion Tools, for example `convert.jpg_to_pdf` or `convert.xml_to_excel`. |
| `options` | body | `object` | yes | Task options object. Include the required conversion inputs such as `file_id` or `url`, plus any conversion-specific settings. Set `sandbox` to `true` for a free provider-side test run. |
| `callbackUrl` | body | `string` | no | Optional HTTPS endpoint that Conversion Tools should call when the task completes. |
