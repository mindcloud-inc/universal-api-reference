# Get Tenant Details with Hasura

Retrieves tenant details from Hasura Cloud.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/graphql`
- **Base URL:** `https://data.pro.hasura.io`
- **Official documentation:** [Get Tenant Details](https://hasura.io/docs/2.0/api-reference/cloud-api-reference/#get-tenant-details)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.tenantId` | body | `string` | yes | Hasura Cloud tenant ID. |
