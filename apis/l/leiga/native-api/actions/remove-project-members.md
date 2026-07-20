# Remove Project Members with Leiga

Removes members from a project in Leiga.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/user/remove-members`
- **Base URL:** `https://app.leiga.com/openapi/api`
- **Official documentation:** [Remove Project Members](https://share.apidog.com/5a741107-c211-410f-880c-048d1917c984/api-3741815.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userIds[]` | body | `array<number>` | yes | User ID List |
| `projectId` | body | `number` | yes | Project ID |
