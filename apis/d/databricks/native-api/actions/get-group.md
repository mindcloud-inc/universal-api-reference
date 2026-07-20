# Get Group with Databricks

Retrieves a group from the Databricks account.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/2.0/accounts/{accountId}/scim/v2/Groups/:groupId`
- **Base URL:** `https://accounts.cloud.databricks.com`
- **Official documentation:** [Get Group](https://docs.databricks.com/api/account/accountgroups/get)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/scim+json` |
| `Content-Type` | `application/scim+json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique ID for a group in the Databricks account. |
