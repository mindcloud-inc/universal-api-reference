# Start anonymization with Neon

Starts anonymization for a branch in Neon.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:project_id/branches/:branch_id/anonymize`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Start anonymization](https://api-docs.neon.tech/reference/startanonymization)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `branch_id` | path | `string` | yes | Neon API parameter branch_id |
