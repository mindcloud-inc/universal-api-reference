# Get Organization Member with ClickHouse

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/organizations/[:organizationId]/members/[:userId]`
- **Base URL:** `https://api.clickhouse.cloud`
- **Official documentation:** [Get Organization Member](https://api.clickhouse.cloud/v1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `string` | yes | ID of the requested organization. |
| `userId` | path | `string` | yes | ID of the requested organization member. |
