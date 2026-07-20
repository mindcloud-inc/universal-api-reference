# List VPC endpoints across all regions with Neon

Retrieves VPC endpoints across all regions from Neon.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:org_id/vpc/vpc_endpoints`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [List VPC endpoints across all regions](https://api-docs.neon.tech/reference/listorganizationvpcendpointsallregions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `org_id` | path | `string` | yes | Neon API parameter org_id |
