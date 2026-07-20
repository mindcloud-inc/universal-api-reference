# Create Tasks for Many Assignees with Jostle

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/tasks/duplicate`
- **Base URL:** `https://api-prod.jostle.us`
- **Official documentation:** [Create Tasks for Many Assignees](https://api.jostle.me/reference/duplicatetasks-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | Title of the task |
| `description` | body | `string` | no | Description of the task |
| `assignees.users[].userId` | body | `string` | no | Id of a user who should receive a duplicated task |
| `assignees.users[].username` | body | `string` | no | Username of a user who should receive a duplicated task |
| `assignees.presetId` | body | `string` | no | Preset list used to select assignees |
