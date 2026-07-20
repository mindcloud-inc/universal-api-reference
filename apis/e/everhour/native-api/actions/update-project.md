# Update Project with Everhour

Updates an existing project in Everhour.

## Endpoint

- **Method:** `PUT`
- **Path:** `/projects/:projectId`
- **Base URL:** `https://api.everhour.com`
- **Official documentation:** [Update Project](https://everhour.docs.apiary.io/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Everhour project ID. |
| `name` | body | `string` | yes | Project name. |
| `type` | body | `string` | yes | Project type. |
| `users[]` | body | `array<number>` | no | Assigned user IDs. |
