# Group Files with Sunwise

Groups project files for bulk creation in Sunwise.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/group-files`
- **Base URL:** `https://production.sunwise.ai/boty/api/v1`
- **Official documentation:** [Group Files](https://production.sunwise.ai/boty/docs)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `files` | body | `file<file>` | yes |
| `pre_group_files` | body | `boolean` | no |
