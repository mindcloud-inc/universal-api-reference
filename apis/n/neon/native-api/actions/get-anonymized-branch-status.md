# Get anonymized branch status with Neon

Retrieves anonymized branch status from Neon.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:project_id/branches/:branch_id/anonymized_status`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Get anonymized branch status](https://api-docs.neon.tech/reference/getanonymizedbranchstatus)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `branch_id` | path | `string` | yes | Neon API parameter branch_id |
