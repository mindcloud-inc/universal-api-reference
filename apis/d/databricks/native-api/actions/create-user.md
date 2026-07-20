# Create User with Databricks

Creates a new user in the Databricks account.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/2.0/accounts/{accountId}/scim/v2/Users`
- **Base URL:** `https://accounts.cloud.databricks.com`
- **Official documentation:** [Create User](https://docs.databricks.com/api/account/accountusers/create)

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
| `displayName` | body | `string` | no | String that represents a concatenation of given and family names. For example `John Smith`. |
| `emails` | body | `list<string>` | yes | All the emails associated with the Databricks user. |
| `$ref` | body | `string` | no | — |
| `emails[].display` | body | `string` | no | — |
| `emails[].primary` | body | `boolean` | no | — |
| `emails[].type` | body | `string` | no | — |
| `emails[].value` | body | `string` | no | — |
| `externalId` | body | `string` | no | External ID is not currently supported. It is reserved for future use. |
| `id` | body | `string` | no | Databricks user ID. |
| `name` | body | `object` | no | — |
| `familyName` | body | `string` | no | Family name of the Databricks user. |
| `givenName` | body | `string` | no | Given name of the Databricks user. |
| `roles` | body | `list<string>` | yes | Indicates if the group has the admin role. |
| `$ref` | body | `string` | no | — |
| `roles[].display` | body | `string` | no | — |
| `roles[].primary` | body | `boolean` | no | — |
| `roles[].type` | body | `string` | no | — |
| `roles[].value` | body | `string` | no | — |
| `userName` | body | `string` | no | Email address of the Databricks user. |
