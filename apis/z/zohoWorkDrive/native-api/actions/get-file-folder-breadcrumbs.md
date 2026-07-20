# Get File/Folder Breadcrumbs with Zoho WorkDrive

Retrieves file or folder breadcrumbs from Zoho WorkDrive.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/files/:resourceId/breadcrumbs`
- **Base URL:** `{api_domain}/workdrive`
- **Official documentation:** [Get File/Folder Breadcrumbs](https://workdrive.zoho.com/apidocs/v1/filesfolders/getfilefolderbreadcrumbs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `resourceId` | path | `string` | yes | The file or folder resource ID. |
