# Update Tenant ENV Vars with Hasura

Updates tenant environment variables in Hasura Cloud.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/graphql`
- **Base URL:** `https://data.pro.hasura.io`
- **Official documentation:** [Update Tenant ENV Vars](https://hasura.io/docs/2.0/api-reference/cloud-api-reference/#update-env-vars)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.tenantId` | body | `string` | yes | Hasura Cloud tenant ID. |
| `variables.currentHash` | body | `string` | yes | Current environment hash from Get Tenant ENV Vars. |
| `variables.envs[]` | body | `array<object>` | yes | Replacement environment variables as objects with key and value fields. |
