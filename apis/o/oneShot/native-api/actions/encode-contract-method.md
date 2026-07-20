# Encode Contract Method with 1Shot

Encodes contract method input data in 1Shot API.

## Endpoint

- **Method:** `POST`
- **Path:** `/methods/:contractMethodId/encode`
- **Base URL:** `https://api.1shotapi.com/v0`
- **Official documentation:** [Encode Contract Method](https://docs.1shotapi.com/api/openapi.html)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `contractMethodId` | path | `string` | yes |
| `params` | body | `object` | no |
