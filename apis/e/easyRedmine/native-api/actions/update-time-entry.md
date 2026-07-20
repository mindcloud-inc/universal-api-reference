# Update Time Entry with Easy Redmine

Updates an existing time entry in Easy Redmine.

## Endpoint

- **Method:** `PUT`
- **Path:** `/time_entries/:id.json`
- **Base URL:** `https://3f73561b8b.bigus-e5.easy8.com`
- **Official documentation:** [Update Time Entry](https://3f73561b8b.bigus-e5.easy8.com/easy_swagger.yml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | ID of the time entry to update. |
| `time_entry` | body | `object` | yes | Time entry payload to update. |
