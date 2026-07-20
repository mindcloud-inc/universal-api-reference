# Delete Reminders with Amazing Marvin

Deletes reminders from Amazing Marvin.

## Endpoint

- **Method:** `POST`
- **Path:** `/reminder/delete`
- **Base URL:** `https://serv.amazingmarvin.com/api`
- **Official documentation:** [Delete Reminders](https://github.com/amazingmarvin/MarvinAPI/wiki/Marvin-API#delete-one-or-more-reminders)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `reminderIds[]` | body | `array<string>` | yes | IDs of reminders to delete. |
