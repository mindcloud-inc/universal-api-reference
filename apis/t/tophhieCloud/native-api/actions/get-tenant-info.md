# Get Tenant Info with Tophhie Cloud

## Endpoint

- **Method:** `GET`
- **Path:** `/tenantinfo`
- **Base URL:** `https://api.tophhie.cloud`
- **Official documentation:** [Get Tenant Info](https://api.tophhie.cloud/swagger/v1/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tenantId` | query | `string` | no | The Entra ID Tenant ID. |
| `domainName` | query | `string` | no | A domain within the Entra ID Tenant. |
| `customDomainsOnly` | query | `boolean` | no | If true, only custom domains are analyzed. |
| `skipEmailConfig` | query | `boolean` | no | If true, omits emailConfiguration and MX records. |
