# Get API Key with ClickHouse

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/organizations/[:organizationId]/keys/[:keyId]`
- **Base URL:** `https://api.clickhouse.cloud`
- **Official documentation:** [Get API Key](https://api.clickhouse.cloud/v1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `string` | yes | ID of the requested organization. |
| `keyId` | path | `string` | yes | ID of the requested API key. |
