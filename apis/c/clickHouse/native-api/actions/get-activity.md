# Get Activity with ClickHouse

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/organizations/[:organizationId]/activities/[:activityId]`
- **Base URL:** `https://api.clickhouse.cloud`
- **Official documentation:** [Get Activity](https://api.clickhouse.cloud/v1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `string` | yes | ID of the requested organization. |
| `activityId` | path | `string` | yes | ID of the requested activity. |
