# Retrieve VPC endpoint details with Neon

Retrieves VPC endpoint details from Neon.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:org_id/vpc/region/:region_id/vpc_endpoints/:vpc_endpoint_id`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Retrieve VPC endpoint details](https://api-docs.neon.tech/reference/getorganizationvpcendpointdetails)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `org_id` | path | `string` | yes | Neon API parameter org_id |
| `region_id` | path | `string` | yes | Neon API parameter region_id |
| `vpc_endpoint_id` | path | `string` | yes | Neon API parameter vpc_endpoint_id |
