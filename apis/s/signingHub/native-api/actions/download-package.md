# Download Package with SigningHub

Downloads a package from SigningHub.

## Endpoint

- **Method:** `GET`
- **Path:** `/v4/packages/:packageId`
- **Base URL:** `https://api.signinghub.com`
- **Official documentation:** [Download Package](https://manuals.nsignhub.com/latest/Api/#tag/Document-Package/operation/V4_Package_DownloadPackageBytes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `packageId` | path | `number` | yes | Package ID of the document package to download. |
