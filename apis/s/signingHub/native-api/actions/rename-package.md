# Rename Package with SigningHub

Renames a package in SigningHub.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v4/packages/:packageId`
- **Base URL:** `https://api.signinghub.com`
- **Official documentation:** [Rename Package](https://manuals.nsignhub.com/latest/Api/#tag/Document-Package/operation/V4_Package_RenamePackage)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `packageId` | path | `number` | yes | The document package to rename. |
| `package_name` | body | `string` | yes | The new package name. |
