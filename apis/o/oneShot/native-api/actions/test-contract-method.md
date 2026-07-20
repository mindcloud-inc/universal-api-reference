# Test Contract Method with 1Shot

Tests a contract method endpoint in 1Shot API.

## Endpoint

- **Method:** `POST`
- **Path:** `/methods/:contractMethodId/test`
- **Base URL:** `https://api.1shotapi.com/v0`
- **Official documentation:** [Test Contract Method](https://docs.1shotapi.com/api/openapi.html)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `contractMethodId` | path | `string` | yes |
| `params` | body | `object` | no |
