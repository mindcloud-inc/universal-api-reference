# List board tasks with Platrum

Retrieves tasks from a Platrum board.

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks/api/board/task/list`
- **Base URL:** `https://3e8e7be.platrum.com`
- **Official documentation:** [List board tasks](http://api.docs.platrum.ru/modules/tasks/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `board_id` | body | `number` | yes | Board ID to list tasks for. |
