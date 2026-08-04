# List Client Info with D-Tools SI

Get clients published by a SI user.

## Endpoint

- **Method:** `GET`
- **Path:** `Subscribe/Clients?includeImported={includeImported}&searchText={searchText}&includeDeleted={includeDeleted}&pageNumber={pageNumber}&pageSize={pageSize}`
- **Base URL:** `https://api.d-tools.com/SI/`

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `clientInfos` | path | `object` | no |
| `clientInfos.email` | query | `string` | no |
| `clientInfos.deleted` | query | `string` | no |
| `clientInfos.phone` | query | `string` | no |
| `clientInfos.id` | query | `string` | no |
| `clientInfos.name` | query | `string` | no |
