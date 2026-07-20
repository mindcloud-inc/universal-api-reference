# Mark Task Done with Amazing Marvin

Marks a task done in Amazing Marvin.

## Endpoint

- **Method:** `POST`
- **Path:** `/markDone`
- **Base URL:** `https://serv.amazingmarvin.com/api`
- **Official documentation:** [Mark Task Done](https://github.com/amazingmarvin/MarvinAPI/wiki/Marvin-API#mark-a-task-done)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `itemId` | body | `string` | yes | Task ID to mark done. |
| `timeZoneOffset` | body | `number` | yes | Timezone offset in minutes. |
