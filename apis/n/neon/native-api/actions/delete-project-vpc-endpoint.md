# Delete VPC endpoint restriction with Neon

Deletes a VPC endpoint restriction from Neon.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/projects/:project_id/vpc_endpoints/:vpc_endpoint_id`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Delete VPC endpoint restriction](https://api-docs.neon.tech/reference/deleteprojectvpcendpoint)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `vpc_endpoint_id` | path | `string` | yes | Neon API parameter vpc_endpoint_id |
