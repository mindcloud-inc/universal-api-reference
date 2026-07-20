# Bulk Create Projects No Files with Sunwise

Creates multiple projects without files in Sunwise.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/bulk-create-no-files`
- **Base URL:** `https://production.sunwise.ai/boty/api/v1`
- **Official documentation:** [Bulk Create Projects No Files](https://production.sunwise.ai/boty/docs)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `contact_id` | body | `string` | yes |
| `project_names[]` | body | `array<string>` | yes |
