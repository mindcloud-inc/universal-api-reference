# Delete Tenant with Hasura

Deletes a tenant from Hasura Cloud.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/graphql`
- **Base URL:** `https://data.pro.hasura.io`
- **Official documentation:** [Delete Tenant](https://hasura.io/docs/2.0/api-reference/cloud-api-reference/#delete-a-tenant)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.tenantId` | body | `string` | yes | Hasura Cloud tenant ID to delete. |
