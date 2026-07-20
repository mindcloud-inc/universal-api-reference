# Create Project with Everhour

Creates a new project in Everhour.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects`
- **Base URL:** `https://api.everhour.com`
- **Official documentation:** [Create Project](https://everhour.docs.apiary.io/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Project name. |
| `type` | body | `string` | yes | Project type. |
| `users[]` | body | `array<number>` | no | Assigned user IDs. |
