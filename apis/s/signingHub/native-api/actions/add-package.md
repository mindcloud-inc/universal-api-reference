# Add Package with SigningHub

Creates a package in SigningHub.

## Endpoint

- **Method:** `POST`
- **Path:** `/v4/packages`
- **Base URL:** `https://api.signinghub.com`
- **Official documentation:** [Add Package](https://manuals.nsignhub.com/latest/Api/#tag/Document-Package/operation/V4_Package_AddPackage)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `package_name` | body | `string` | no | The name of the package. Defaults to Untitled when omitted. |
| `workflow_mode` | body | `string` | no | Controls whether the workflow is for me only, others only, or me and others. |
| `folder_name` | body | `string` | no | Optional folder name to upload the package into an existing custom or shared folder. |
