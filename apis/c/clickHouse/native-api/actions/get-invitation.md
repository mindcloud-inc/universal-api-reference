# Get Invitation with ClickHouse

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/organizations/[:organizationId]/invitations/[:invitationId]`
- **Base URL:** `https://api.clickhouse.cloud`
- **Official documentation:** [Get Invitation](https://api.clickhouse.cloud/v1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `string` | yes | ID of the requested organization. |
| `invitationId` | path | `string` | yes | ID of the requested invitation. |
