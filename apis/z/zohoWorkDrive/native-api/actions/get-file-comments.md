# Get File Comments with Zoho WorkDrive

Retrieves comments for a Zoho WorkDrive file.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/files/:resourceId/comments`
- **Base URL:** `{api_domain}/workdrive`
- **Official documentation:** [Get File Comments](https://workdrive.zoho.com/apidocs/v1/filesfolders/getfilecomments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `resourceId` | path | `string` | yes | The file or folder resource ID. |
