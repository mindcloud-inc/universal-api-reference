# Create Group with Databricks

Creates a new group in the Databricks account.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/2.0/accounts/{accountId}/scim/v2/Groups`
- **Base URL:** `https://accounts.cloud.databricks.com`
- **Official documentation:** [Create Group](https://docs.databricks.com/api/account/accountgroups/create)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/scim+json` |
| `Content-Type` | `application/scim+json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `displayName` | body | `string` | no | String that represents a human-readable group name |
| `externalId` | body | `string` | no | — |
| `id` | body | `string` | no | Databricks group ID |
| `members` | body | `list<string>` | yes | — |
| `$ref` | body | `string` | no | — |
| `members[].display` | body | `string` | no | — |
| `members[].primary` | body | `boolean` | no | — |
| `members[].type` | body | `string` | no | — |
| `members[].value` | body | `string` | no | — |
| `roles` | body | `list<string>` | yes | Indicates if the group has the admin role. |
| `$ref` | body | `string` | no | — |
| `roles[].display` | body | `string` | no | — |
| `roles[].primary` | body | `boolean` | no | — |
| `roles[].type` | body | `string` | no | — |
| `roles[].value` | body | `string` | no | — |
