# Get Tenant ENV Vars with Hasura

Retrieves tenant environment variables from Hasura Cloud.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/graphql`
- **Base URL:** `https://data.pro.hasura.io`
- **Official documentation:** [Get Tenant ENV Vars](https://hasura.io/docs/2.0/api-reference/cloud-api-reference/#get-env-vars)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.tenantId` | body | `string` | yes | Hasura Cloud tenant ID. |
