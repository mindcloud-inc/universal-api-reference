# Archive or Unarchive Project with Everhour

Archives or unarchives a project in Everhour.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/projects/:projectId/archive`
- **Base URL:** `https://api.everhour.com`
- **Official documentation:** [Archive or Unarchive Project](https://everhour.docs.apiary.io/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Everhour project ID. |
| `archived` | body | `boolean` | yes | Whether the project should be archived. |
