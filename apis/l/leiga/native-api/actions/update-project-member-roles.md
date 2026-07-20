# Update Project Member Roles with Leiga

Updates project member roles in Leiga.

## Endpoint

- **Method:** `POST`
- **Path:** `/project/role-change`
- **Base URL:** `https://app.leiga.com/openapi/api`
- **Official documentation:** [Update Project Member Roles](https://share.apidog.com/5a741107-c211-410f-880c-048d1917c984/api-3741822.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `roleIdList[]` | body | `array<number>` | yes | Role ID List |
| `projectId` | body | `number` | yes | Project ID |
| `userId` | body | `number` | yes | User ID |
