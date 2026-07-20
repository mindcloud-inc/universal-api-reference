# List Tasks with Paymo

Retrieves tasks from Paymo.

## Endpoint

- **Method:** `GET`
- **Path:** `tasks`
- **Base URL:** `https://app.paymoapp.com/api/`
- **Official documentation:** [List Tasks](https://github.com/paymo-org/api/blob/master/sections/tasks.md#getting-tasks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `where` | query | `string` | no | Optional raw Paymo filtering expression, for example `tasklist_id=7096346`. |
