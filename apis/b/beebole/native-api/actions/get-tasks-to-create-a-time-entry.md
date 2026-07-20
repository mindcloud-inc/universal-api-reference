# Get Tasks to Create a Time Entry with Beebole

Retrieves tasks for creating a time entry in Beebole.

## Endpoint

- **Method:** `POST`
- **Base URL:** `https://beebole-apps.com/api/v2`
- **Official documentation:** [Get Tasks to Create a Time Entry](https://beebole.com/help/api#get-tasks-to-create-a-time-entry)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subproject.id` | body | `number` | yes | The Beebole subproject identifier whose available tasks should be listed. |
| `project.id` | body | `number` | no | Optional project identifier used when tasks are configured directly on a project in the connected account. |
| `date` | body | `string` | yes | The date used by Beebole to evaluate which tasks are available. |
