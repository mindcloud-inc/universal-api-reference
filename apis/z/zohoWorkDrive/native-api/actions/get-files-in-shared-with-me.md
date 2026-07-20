# Get Files in Shared with Me with Zoho WorkDrive

Retrieves files shared with a Zoho WorkDrive user.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/users/:teamMemberId/incomingfiles`
- **Base URL:** `{api_domain}/workdrive`
- **Official documentation:** [Get Files in Shared with Me](https://workdrive.zoho.com/apidocs/v1/teammemberfiles/getfilesinsharedwithme)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamMemberId` | path | `string` | yes | The team member ID. |
| `filter[type]` | query | `string` | no | Filter the results by resource type. |
| `filter[user]` | query | `string` | no | Filter by the sharing user. |
| `filter[group]` | query | `string` | no | Filter by the sharing group. |
| `page[limit]` | query | `string` | no | Maximum number of records to return. |
| `page[offset]` | query | `string` | no | Number of records to skip before returning results. |
| `sort` | query | `string` | no | Sort expression for the returned resources. |
