# Duplicate a task with Asana

Duplicates a task in Asana.

## Endpoint

- **Method:** `POST`
- **Path:** `tasks/:task_gid/duplicate`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Duplicate a task](https://developers.asana.com/reference/duplicatetask)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.include` | body | `string` | yes | — |
| `data.name` | body | `string` | yes | — |
| `opt_fields[]` | query | `array<string>` | no | — |
| `task_gid` | path | `string` | yes | Path parameter: task_gid |
| `data` | body | `object` | yes | — |
