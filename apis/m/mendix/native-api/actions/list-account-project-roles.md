# List Account Project Roles with Mendix

Retrieves project roles for an account in Mendix.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:accountId/roles`
- **Base URL:** `https://projects-api.home.mendix.com/v2`
- **API:** rest
- **Official documentation:** [List Account Project Roles](https://docs.mendix.com/apidocs-mxsdk/apidocs/projects-api/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account-id` | path | `string` | yes | The unique identifier of the account or company. |
| `changedSince` | query | `date` | no | Only return roles created or changed since this ISO 8601 date and time. |
