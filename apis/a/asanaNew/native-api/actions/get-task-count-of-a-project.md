# Get task count of a project with Asana

Retrieves a project's task count from Asana.

## Endpoint

- **Method:** `GET`
- **Path:** `projects/:project_gid/task_counts`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Get task count of a project](https://developers.asana.com/reference/gettaskcountsforproject)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_gid` | path | `string` | yes | Asana project gid parameter. |
| `opt_pretty` | query | `boolean` | no | Asana opt pretty parameter. |
| `opt_fields` | query | `list<string>` | no | Asana opt fields parameter. Send multiple values as a array. |
