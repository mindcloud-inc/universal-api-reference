# Create Table with Extruct AI

Creates a table in Extruct AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/tables`
- **Base URL:** `https://api.extruct.ai`
- **Official documentation:** [Create Table](https://docs.extruct.ai/api-reference/tables/create-table)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Table name. Defaults to Untitled Table. |
| `description` | body | `string` | no | Optional table description. |
| `tags[]` | body | `array<string>` | no | Optional list of table tags. |
| `kind` | body | `string` | no | Table kind. Defaults to company. Accepted values: `0`, `1`, `2`. |
| `column_configs[]` | body | `array<object>` | no | Optional initial column definitions. |
