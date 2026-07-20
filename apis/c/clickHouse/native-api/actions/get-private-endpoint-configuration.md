# Get Private Endpoint Configuration with ClickHouse

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/organizations/[:organizationId]/services/[:serviceId]/privateEndpointConfig`
- **Base URL:** `https://api.clickhouse.cloud`
- **Official documentation:** [Get Private Endpoint Configuration](https://api.clickhouse.cloud/v1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `string` | yes | ID of the organization that owns the service. |
| `serviceId` | path | `string` | yes | ID of the requested service. |
