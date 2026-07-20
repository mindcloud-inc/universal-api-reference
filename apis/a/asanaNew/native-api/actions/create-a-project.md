# Create a project with Asana

Creates a project in Asana.

## Endpoint

- **Method:** `POST`
- **Path:** `projects`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Create a project](https://developers.asana.com/reference/createproject)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `color` | body | `string` | no | — |
| `defaultView` | body | `string` | no | — |
| `due_date` | body | `string` | no | — |
| `due_on` | body | `string` | no | — |
| `is_template` | body | `boolean` | no | — |
| `name` | body | `string` | no | — |
| `notes` | body | `string` | no | — |
| `owner` | body | `string` | no | — |
| `public` | body | `boolean` | no | — |
| `start_on` | body | `string` | no | — |
| `team` | body | `string` | no | — |
| `workspace` | body | `string` | no | — |
| `opt_pretty` | query | `boolean` | no | Asana opt pretty parameter. |
| `opt_fields` | query | `list<string>` | no | Asana opt fields parameter. |
