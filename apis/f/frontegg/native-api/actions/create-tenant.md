# Create Tenant with Frontegg

Creates a new account in Frontegg.

## Endpoint

- **Method:** `POST`
- **Path:** `/tenants/resources/tenants/v1`
- **Base URL:** `https://api.frontegg.com`
- **Official documentation:** [Create Tenant](https://developers.frontegg.com/ciam/api/tenants/accounts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Account (tenant) name. |
| `tenantId` | body | `string` | no | Optional unique tenant ID; Frontegg auto-generates one when omitted. |
| `creatorName` | body | `string` | no | Optional creator name for the tenant. |
| `creatorEmail` | body | `string` | no | Optional creator email for the tenant. |
