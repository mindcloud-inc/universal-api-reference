# Enable Service For Sub-Tenant with Acronis

Enables a service for a sub-tenant in Acronis.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/2/applications/{application_id}/bindings/tenants/{tenant_id}`
- **Base URL:** `{dataCenterUrl}`
- **Official documentation:** [Enable Service For Sub-Tenant](https://developer.acronis.com/doc/outbound/apis/api-library/account/services/enabling-service.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `application_id` | path | `string` | yes | Application Id path parameter. |
| `tenant_id` | path | `string` | yes | Tenant Id path parameter. |
