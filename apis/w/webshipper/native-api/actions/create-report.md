# Create Report with Webshipper

Creates a report in Webshipper.

## Endpoint

- **Method:** `POST`
- **Path:** `/reports`
- **Base URL:** `https://{accountName}.api.webshipper.io/v2`
- **Official documentation:** [Create Report](https://docs.webshipper.io/#reports)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.attributes.end_time` | body | `string` | no | Report end time in ISO-8601 format. |
| `data.attributes.output_formats` | body | `string` | no | Output formats to generate. |
| `data.attributes.start_time` | body | `string` | no | Report start time in ISO-8601 format. |
| `data.relationships.report_type.data.id` | body | `string` | no | Report type ID. |
| `data.type` | body | `string` | yes | Use the default value `reports`. |
| `data.relationships.report_type.data.type` | body | `string` | yes | Use the default value `report_types`. |
