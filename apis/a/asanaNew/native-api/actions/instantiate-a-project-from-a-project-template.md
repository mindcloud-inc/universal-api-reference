# Instantiate a project from a project template with Asana

Creates a project from an Asana project template.

## Endpoint

- **Method:** `POST`
- **Path:** `project_templates/:project_template_gid/instantiateProject`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Instantiate a project from a project template](https://developers.asana.com/reference/instantiateproject)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `data.is_strict` | body | `boolean` | no |
| `data.name` | body | `string` | no |
| `data.public` | body | `boolean` | no |
| `data.requested_dates[]` | body | `array` | no |
| `data.requested_dates[].gid` | body | `string` | no |
| `data.requested_dates[].value` | body | `date` | no |
| `data.team` | body | `string` | no |
| `data.workspace` | body | `string` | no |
| `project_template_gid` | path | `string` | yes |
| `opt_pretty` | query | `boolean` | no |
| `opt_fields` | query | `list<string>` | no |
