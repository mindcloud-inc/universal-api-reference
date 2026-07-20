# Remove task with Platrum

Deletes a task from Platrum.

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks/api/task/remove`
- **Base URL:** `https://3e8e7be.platrum.com`
- **Official documentation:** [Remove task](http://api.docs.platrum.ru/modules/tasks/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `number` | yes | Task ID to remove. |
| `is_edit_further` | body | `boolean` | no | Delete linked recurring tasks. |
