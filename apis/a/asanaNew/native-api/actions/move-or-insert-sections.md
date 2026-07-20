# Move or Insert sections with Asana

Moves or inserts sections in an Asana project.

## Endpoint

- **Method:** `POST`
- **Path:** `projects/:project_gid/sections/insert`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Move or Insert sections](https://developers.asana.com/reference/insertsectionforproject)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.after_section` | body | `string` | yes | — |
| `data.before_section` | body | `string` | yes | — |
| `data.project` | body | `string` | yes | — |
| `data.section` | body | `string` | yes | — |
| `project_gid` | path | `string` | yes | Asana project gid parameter. |
| `opt_pretty` | query | `boolean` | no | Asana opt pretty parameter. |
| `data.section` | body | `string` | yes | Asana section parameter. |
| `data.before_section` | body | `string` | no | Asana before section parameter. |
| `data.after_section` | body | `string` | no | Asana after section parameter. |
