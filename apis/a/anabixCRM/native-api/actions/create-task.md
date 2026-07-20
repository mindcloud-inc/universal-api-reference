# Create Task with Anabix CRM

Creates a new task in Anabix CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/api`
- **Base URL:** `https://app.anabix.cz`
- **Official documentation:** [Create Task](https://www.anabix.cz/wp-content/uploads/2025/02/anabix_api_manual-2025.pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `string` | yes | Task body. Anabix requires body when creating a task. |
| `idContact` | body | `number` | no | Optional related contact ID for the task. |
| `title` | body | `string` | no | Optional task title. If omitted, Anabix creates a title from the task body. |
