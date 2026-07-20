# Set the parent of a task with Asana

Sets a task's parent in Asana.

## Endpoint

- **Method:** `POST`
- **Path:** `tasks/:task_gid/setParent`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Set the parent of a task](https://developers.asana.com/reference/setparentfortask)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.insert_after` | body | `string` | yes | — |
| `data.insert_before` | body | `string` | yes | — |
| `data.parent` | body | `string` | yes | — |
| `task_gid` | path | `string` | yes | Asana task gid parameter. |
| `opt_pretty` | query | `boolean` | no | Asana opt pretty parameter. |
| `opt_fields` | query | `list<string>` | no | Asana opt fields parameter. |
| `data.parent` | body | `string` | yes | Asana parent parameter. |
| `data.insert_after` | body | `string` | no | Asana insert after parameter. |
| `data.insert_before` | body | `string` | no | Asana insert before parameter. |
