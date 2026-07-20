# Duplicate a project with Asana

Duplicates a project in Asana.

## Endpoint

- **Method:** `POST`
- **Path:** `projects/:project_gid/duplicate`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Duplicate a project](https://developers.asana.com/reference/duplicateproject)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.include` | body | `string` | no | — |
| `data.name` | body | `string` | no | — |
| `data.schedule_dates.due_on` | body | `string` | no | — |
| `data.schedule_dates.should_skip_weekends` | body | `boolean` | no | — |
| `data.schedule_dates.start_on` | body | `string` | no | — |
| `data.team` | body | `string` | no | — |
| `project_gid` | path | `string` | yes | Asana project gid parameter. |
| `opt_pretty` | query | `boolean` | no | Asana opt pretty parameter. |
| `opt_fields` | query | `list<string>` | no | Asana opt fields parameter. |
| `data.name` | body | `string` | yes | Asana name parameter. |
| `data.team` | body | `string` | no | Asana team parameter. |
| `data.include` | body | `string` | no | Asana include parameter. |
