# Get Service Principal with Databricks

Retrieves a service principal from the Databricks account.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/2.0/accounts/{accountId}/scim/v2/ServicePrincipals/:servicePrincipalId`
- **Base URL:** `https://accounts.cloud.databricks.com`
- **Official documentation:** [Get Service Principal](https://docs.databricks.com/api/account/accountserviceprincipals/get)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/scim+json` |
| `Content-Type` | `application/scim+json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique ID for a service principal in the Databricks account. |
