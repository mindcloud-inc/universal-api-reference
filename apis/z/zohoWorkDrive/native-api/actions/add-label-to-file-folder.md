# Add Label to File/Folder with Zoho WorkDrive

Adds a label to a Zoho WorkDrive file or folder.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/labels/:labelId/relationships/files`
- **Base URL:** `{api_domain}/workdrive`
- **Official documentation:** [Add Label to File/Folder](https://workdrive.zoho.com/apidocs/v1/labels/addlabeltofilefolder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `labelId` | path | `string` | yes | The label ID to assign. |
| `data[].id` | body | `string` | yes | The resource ID to associate with the label. |
| `data[].attributes.resource_id` | body | `string` | no | Optional nested resource ID field from the published WorkDrive example payload. |
