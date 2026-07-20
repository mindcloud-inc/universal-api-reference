# Get Recent Files with Zoho WorkDrive

Retrieves recent files from Zoho WorkDrive.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/users/:teamMemberId/recentfiles`
- **Base URL:** `{api_domain}/workdrive`
- **Official documentation:** [Get Recent Files](https://workdrive.zoho.com/apidocs/v1/teammemberfiles/getrecentfiles)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamMemberId` | path | `string` | yes | The team member ID. |
| `filter[type]` | query | `string` | no | Filter the results by resource type. |
| `page[limit]` | query | `string` | no | Maximum number of records to return. |
| `page[offset]` | query | `string` | no | Number of records to skip before returning results. |
