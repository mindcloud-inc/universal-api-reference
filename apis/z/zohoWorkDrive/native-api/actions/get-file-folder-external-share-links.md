# Get File/Folder External Share Links with Zoho WorkDrive

Retrieves external share links for a Zoho WorkDrive file or folder.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/files/:resourceId/links`
- **Base URL:** `{api_domain}/workdrive`
- **Official documentation:** [Get File/Folder External Share Links](https://workdrive.zoho.com/apidocs/v1/filesfolders/getfilefolderexternalsharelinks)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `resourceId` | path | `string` | yes | The file or folder resource ID. |
| `filter[type]` | query | `string` | no | Filter the returned share links by type. |
