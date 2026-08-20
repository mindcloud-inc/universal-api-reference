# Get Task with Centerpoint

## Endpoint

- **Method:** `GET`
- **Path:** `tasks/:TASK_ID`
- **Base URL:** `https://api.centerpointconnect.io/centerpoint/`
- **Official documentation:** [Get Task](https://api-portal.centerpointconnect.io/portal/catalogue-products/centerpoint-api-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/tasks/TASK_IDGET)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `TASK_ID` | path | `number` | yes |
| `fields[profiles]` | query | `string` | no |
| `fields[employees]` | query | `string` | no |
| `fields[companies]` | query | `string` | no |
| `fields[properties]` | query | `string` | no |
| `fields[productions]` | query | `string` | no |
| `include` | query | `string` | no |
