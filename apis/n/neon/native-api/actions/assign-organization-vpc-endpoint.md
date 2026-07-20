# Assign or update VPC endpoint with Neon

Assigns or updates VPC endpoint in Neon.

## Endpoint

- **Method:** `POST`
- **Path:** `/organizations/:org_id/vpc/region/:region_id/vpc_endpoints/:vpc_endpoint_id`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Assign or update VPC endpoint](https://api-docs.neon.tech/reference/assignorganizationvpcendpoint)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `org_id` | path | `string` | yes | Neon API parameter org_id |
| `region_id` | path | `string` | yes | Neon API parameter region_id |
| `vpc_endpoint_id` | path | `string` | yes | Neon API parameter vpc_endpoint_id |
| `label` | body | `string` | yes | Neon API parameter label |
