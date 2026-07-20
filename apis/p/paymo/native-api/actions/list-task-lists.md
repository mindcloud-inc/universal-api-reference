# List Task Lists with Paymo

Retrieves task lists from Paymo.

## Endpoint

- **Method:** `GET`
- **Path:** `tasklists`
- **Base URL:** `https://app.paymoapp.com/api/`
- **Official documentation:** [List Task Lists](https://github.com/paymo-org/api/blob/master/sections/tasklists.md#getting-task-lists)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `where` | query | `string` | no | Optional raw Paymo filtering expression, for example `project_id=3540359`. |
