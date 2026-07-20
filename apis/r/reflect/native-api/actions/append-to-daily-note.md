# Append to Daily Note with Reflect

Appends text to a daily note in Reflect.

## Endpoint

- **Method:** `PUT`
- **Path:** `/graphs/:graphId/daily-notes`
- **Base URL:** `https://reflect.app/api`
- **Official documentation:** [Append to Daily Note](https://openpm.ai/packages/reflect#/graphs/{graphId}/daily-notes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `graphId` | path | `list<string>` | yes | Your graph identifier |
| `date` | body | `date` | no | Date of the daily note in ISO 8601 format |
| `text` | body | `string` | yes | Text to append to the daily note |
| `list_name` | body | `string` | no | Name of the list to append to |
