# Update Habit with Amazing Marvin

Updates habit history in Amazing Marvin.

## Endpoint

- **Method:** `POST`
- **Path:** `/updateHabit`
- **Base URL:** `https://serv.amazingmarvin.com/api`
- **Official documentation:** [Update Habit](https://github.com/amazingmarvin/MarvinAPI/wiki/Marvin-API#record-a-habit)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `habitId` | body | `string` | yes | Habit identifier to update. |
| `time` | body | `number` | no | Timestamp to record for the habit update. |
| `value` | body | `number` | no | Numeric value to record for the habit update. |
| `undo` | body | `boolean` | no | Set to true to undo the last habit recording. |
| `history[]` | body | `array<number>` | no | Flat array used to rewrite the habit history. |
| `updateDB` | body | `boolean` | no | Set to true to update the Cloudant habit document as well. |
