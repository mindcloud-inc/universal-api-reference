# Move Users Between Tenants with Frontegg

Moves users between accounts in Frontegg.

## Endpoint

- **Method:** `PUT`
- **Path:** `/identity/resources/users/v1/tenants/migrate`
- **Base URL:** `https://api.frontegg.com`
- **Official documentation:** [Move Users Between Tenants](https://developers.frontegg.com/ciam/api/identity/users)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `srcTenantId` | body | `string` | yes | Source tenant ID. |
| `targetTenantId` | body | `string` | yes | Target tenant ID. |
