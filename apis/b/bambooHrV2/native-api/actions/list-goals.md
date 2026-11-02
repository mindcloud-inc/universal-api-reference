# List Goals with BambooHR

Lists goals from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/performance/employees/:employeeId/goals`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [List Goals](https://documentation.bamboohr.com/reference/list-goals)

## Requirements

- **OAuth scopes:** `goal`
- **scope:** `goal` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `employeeId` | path | `string` | yes | The internal employee ID of the employee the goals are assigned to. |
| `filter` | query | `list<string>` | no | Goal status filter. Use `status-inProgress` for current active goals, `status-completed` for completed goals, `status-closed` for closed goals, and `status-all` when locating a goal by title for update/delete/reopen or when the user asks for all goals. If omitted, closed goals are excluded. Unrecognized values behave like omission. Accepted values: `status-all`, `status-closed`, `status-completed`, `status-inProgress`. |
