# Get Usage Costs with ClickHouse

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/organizations/[:organizationId]/usageCost`
- **Base URL:** `https://api.clickhouse.cloud`
- **Official documentation:** [Get Usage Costs](https://api.clickhouse.cloud/v1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `string` | yes | ID of the requested organization. |
| `from_date` | query | `string` | yes | Start date for the report in YYYY-MM-DD format, e.g. 2024-12-19. |
| `to_date` | query | `string` | yes | End date, inclusive, in YYYY-MM-DD format. This date cannot be more than 30 days after from_date. |
