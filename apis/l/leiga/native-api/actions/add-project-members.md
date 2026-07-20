# Add Project Members with Leiga

Adds members to a project in Leiga.

## Endpoint

- **Method:** `POST`
- **Path:** `/user/add-members`
- **Base URL:** `https://app.leiga.com/openapi/api`
- **Official documentation:** [Add Project Members](https://share.apidog.com/5a741107-c211-410f-880c-048d1917c984/api-3741814.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userIds[]` | body | `array<number>` | yes | User ID List |
| `projectId` | body | `number` | yes | Project ID |
