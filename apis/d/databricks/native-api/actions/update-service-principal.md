# Update Service Principal with Databricks

Updates an existing service principal in the Databricks account.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/2.0/accounts/{accountId}/scim/v2/ServicePrincipals/:servicePrincipalId`
- **Base URL:** `https://accounts.cloud.databricks.com`
- **Official documentation:** [Update Service Principal](https://docs.databricks.com/api/account/accountserviceprincipals/patch)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/scim+json` |
| `Content-Type` | `application/scim+json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique ID in the Databricks workspace. |
| `Operations` | body | `list<string>` | yes | — |
| `operations[].op` | body | `string` | no | Type of patch operation. |
| `operations[].path` | body | `string` | no | Selection of patch operation |
| `operations[].value` | body | `string` | no | Value to modify |
| `schemas` | body | `list<string>` | yes | The schema of the patch request. Must be ["urn:ietf:params:scim:api:messages:2.0:PatchOp"]. |
