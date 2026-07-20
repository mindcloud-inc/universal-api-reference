# Update Task with GoDial

Updates an existing task in GoDial.

## Endpoint

- **Method:** `PUT`
- **Path:** `/externals/tasks/[:id]/update`
- **Base URL:** `https://enterprise.godial.cc/meta/api`
- **Official documentation:** [Update Task](https://godial.stoplight.io/docs/godial/b3A6NzQwMTQ0Ng-task-update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Task ID. |
| `name` | body | `string` | yes | Provide new name of the Task |
