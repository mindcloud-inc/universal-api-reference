# Bulk Create Projects With Files with Sunwise

Creates multiple projects from uploaded files in Sunwise.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/bulk-create`
- **Base URL:** `https://production.sunwise.ai/boty/api/v1`
- **Official documentation:** [Bulk Create Projects With Files](https://production.sunwise.ai/boty/docs)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `files` | body | `file<file>` | yes |
| `contact_id` | body | `string` | yes |
| `pre_group_files` | body | `boolean` | no |
| `background_project_stop` | body | `number` | no |
| `project_names_map` | body | `string` | no |
