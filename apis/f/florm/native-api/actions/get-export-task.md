# Get Export Task with Florm

Retrieves a specific Florm export task.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/export/form/:form_guid/task/:task_guid`
- **Base URL:** `https://api.florm.io`
- **Official documentation:** [Get Export Task](https://api.florm.io/docs#/default/get_task_v1_export_form__form_guid__task__task_guid__get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `form_guid` | path | `string` | yes | GUID of the Florm form tied to the export task. |
| `task_guid` | path | `string` | yes | GUID of the Florm export task. |
