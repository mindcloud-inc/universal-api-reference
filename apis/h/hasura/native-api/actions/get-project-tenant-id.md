# Get Project Tenant ID with Hasura

Retrieves a Hasura project tenant ID.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/graphql`
- **Base URL:** `https://data.pro.hasura.io`
- **Official documentation:** [Get Project Tenant ID](https://hasura.io/docs/2.0/api-reference/cloud-api-reference/#get-project-tenant-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.projectId` | body | `string` | yes | Hasura Cloud project ID. |
