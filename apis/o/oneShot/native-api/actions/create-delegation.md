# Create Delegation with 1Shot

Creates a new wallet delegation in 1Shot API.

## Endpoint

- **Method:** `POST`
- **Path:** `/wallets/:walletId/delegations`
- **Base URL:** `https://api.1shotapi.com/v0`
- **Official documentation:** [Create Delegation](https://docs.1shotapi.com/api/openapi.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `walletId` | path | `string` | yes | — |
| `delegationData` | body | `list<string>` | yes | Live provider runtime currently requires delegationData as an array-shaped body value, even though the published OpenAPI documents a single JSON string. Each array element should be one serialized delegation payload string. |
| `startTime` | body | `date` | no | — |
| `endTime` | body | `date` | no | — |
| `contractAddresses` | body | `list<string>` | no | — |
| `methods` | body | `list<string>` | no | — |
