# List VPC endpoints with Neon

Retrieves VPC endpoints from Neon.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:org_id/vpc/region/:region_id/vpc_endpoints`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [List VPC endpoints](https://api-docs.neon.tech/reference/listorganizationvpcendpoints)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `org_id` | path | `string` | yes | Neon API parameter org_id |
| `region_id` | path | `string` | yes | Neon API parameter region_id |
