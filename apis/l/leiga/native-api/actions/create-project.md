# Create Project with Leiga

Creates a new project in Leiga.

## Endpoint

- **Method:** `POST`
- **Path:** `/project/add`
- **Base URL:** `https://app.leiga.com/openapi/api`
- **Official documentation:** [Create Project](https://share.apidog.com/5a741107-c211-410f-880c-048d1917c984/api-3741824.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `templateCode` | body | `string` | yes | Project Template Code |
| `projectName` | body | `string` | yes | Project Name |
| `leaderId` | body | `number` | yes | Project Leader ID |
| `description` | body | `string` | no | Project Description |
