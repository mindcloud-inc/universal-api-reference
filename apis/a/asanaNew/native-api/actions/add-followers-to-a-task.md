# Add followers to a task with Asana

Adds followers to a task in Asana.

## Endpoint

- **Method:** `POST`
- **Path:** `tasks/:task_gid/addFollowers`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Add followers to a task](https://developers.asana.com/reference/addfollowersfortask)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `data.followers[]` | body | `array<string>` | yes |
| `task_gid` | path | `string` | yes |
| `opt_pretty` | query | `boolean` | no |
| `opt_fields` | query | `list<string>` | no |
