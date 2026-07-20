# Create Service Principal with Databricks

Creates a new service principal in the Databricks account.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/2.0/accounts/{accountId}/scim/v2/ServicePrincipals`
- **Base URL:** `https://accounts.cloud.databricks.com`
- **Official documentation:** [Create Service Principal](https://docs.databricks.com/api/account/accountserviceprincipals/create)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/scim+json` |
| `Content-Type` | `application/scim+json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `active` | body | `boolean` | no | If this user is active |
| `applicationId` | body | `string` | no | UUID relating to the service principal |
| `displayName` | body | `string` | no | String that represents a concatenation of given and family names. |
| `externalId` | body | `string` | no | — |
| `id` | body | `string` | no | Databricks service principal ID. |
| `roles` | body | `list<string>` | yes | Indicates if the group has the admin role. |
| `$ref` | body | `string` | no | — |
| `roles[].display` | body | `string` | no | — |
| `roles[].primary` | body | `boolean` | no | — |
| `roles[].type` | body | `string` | no | — |
| `roles[].value` | body | `string` | no | — |
