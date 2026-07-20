# Reopen Task with Runrun.it

Reopens a task in Runrun.it.

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks/:id/reopen`
- **Base URL:** `https://runrun.it/api/v1.0`
- **Official documentation:** [Reopen Task](https://runrun.it/api/documentation#tasks-reopen-a-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Id path parameter. |
| `reopen_or_pause_descendant_tasks` | body | `boolean` | no | Force pause/reopen all descendant tasks |
