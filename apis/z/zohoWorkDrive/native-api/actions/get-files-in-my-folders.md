# Get Files in My Folders with Zoho WorkDrive

Retrieves files and folders from My Folders in Zoho WorkDrive.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/privatespace/:myfolderId/files`
- **Base URL:** `{api_domain}/workdrive`
- **Official documentation:** [Get Files in My Folders](https://workdrive.zoho.com/apidocs/v1/myfoldersfiles/getfilesinmyfolders)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `myfolderId` | path | `string` | yes | The private-space folder ID. |
| `filter[type]` | query | `string` | no | Filter the results by resource type. |
| `filter[extension]` | query | `string` | no | Filter files by extension. |
| `page[limit]` | query | `string` | no | Maximum number of records to return. |
| `page[offset]` | query | `string` | no | Number of records to skip before returning results. |
| `page[next]` | query | `string` | no | Pagination token for the next page of results. |
| `fields[files]` | query | `string` | no | Comma-separated file fields to include in the response. |
| `sort` | query | `string` | no | Sort expression for the returned resources. |
