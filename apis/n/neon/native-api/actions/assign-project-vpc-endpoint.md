# Set VPC endpoint restriction with Neon

Sets a VPC endpoint restriction in Neon.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:project_id/vpc_endpoints/:vpc_endpoint_id`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Set VPC endpoint restriction](https://api-docs.neon.tech/reference/assignprojectvpcendpoint)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `vpc_endpoint_id` | path | `string` | yes | Neon API parameter vpc_endpoint_id |
| `label` | body | `string` | yes | Neon API parameter label |
