# List Account Projects with Mendix

Retrieves company-owned projects for an account in Mendix.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:accountId/projects`
- **Base URL:** `https://projects-api.home.mendix.com/v2`
- **API:** rest
- **Official documentation:** [List Account Projects](https://docs.mendix.com/apidocs-mxsdk/apidocs/projects-api/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account-id` | path | `string` | yes | The unique identifier of the account or company. |
| `createdSince` | query | `date` | no | Only return projects created after this UTC date and time, such as 2020-01-16T05:53:28Z. |
| `categories` | query | `string` | no | Comma-separated categories with values in the documented Mendix filter format. |
