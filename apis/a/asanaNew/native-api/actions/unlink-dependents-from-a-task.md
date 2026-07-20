# Unlink dependents from a task with Asana

Removes dependents from a task in Asana.

## Endpoint

- **Method:** `POST`
- **Path:** `tasks/:task_gid/removeDependents`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Unlink dependents from a task](https://developers.asana.com/reference/removedependentsfortask)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.dependents[]` | body | `array<string>` | yes | — |
| `task_gid` | path | `string` | yes | Asana task gid parameter. |
| `opt_pretty` | query | `boolean` | no | Asana opt pretty parameter. |
| `data.dependents` | body | `list<string>` | no | Asana dependents parameter. |
