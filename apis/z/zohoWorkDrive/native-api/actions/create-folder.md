# Create Folder with Zoho WorkDrive

Creates a new folder in Zoho WorkDrive.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/files`
- **Base URL:** `{api_domain}/workdrive`
- **Official documentation:** [Create Folder](https://workdrive.zoho.com/apidocs/v1/folders/createfolder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.attributes.name` | body | `string` | yes | Name of the folder to create. |
| `data.attributes.parent_id` | body | `string` | yes | Parent folder resource ID where the new folder should be created. |
