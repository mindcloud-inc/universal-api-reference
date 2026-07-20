# Add a project to a task with Asana

Adds a project to a task in Asana.

## Endpoint

- **Method:** `POST`
- **Path:** `tasks/:task_gid/addProject`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Add a project to a task](https://developers.asana.com/reference/addprojectfortask)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.insert_after` | body | `string` | yes | — |
| `data.insert_before` | body | `string` | yes | — |
| `data.project` | body | `string` | yes | — |
| `data.section` | body | `string` | yes | — |
| `task_gid` | path | `string` | yes | Asana task gid parameter. |
| `opt_pretty` | query | `boolean` | no | Asana opt pretty parameter. |
| `data.project` | body | `string` | yes | Asana project parameter. |
| `data.insert_after` | body | `string` | no | Asana insert after parameter. |
| `data.insert_before` | body | `string` | no | Asana insert before parameter. |
| `data.section` | body | `string` | no | Asana section parameter. |
