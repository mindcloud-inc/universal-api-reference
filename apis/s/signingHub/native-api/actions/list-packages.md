# List Packages with SigningHub

Retrieves packages from SigningHub.

## Endpoint

- **Method:** `GET`
- **Path:** `/v4/packages/:document_status/:pageNo/:recordPerPage`
- **Base URL:** `https://api.signinghub.com`
- **Official documentation:** [List Packages](https://manuals.nsignhub.com/latest/Api/#tag/Document-Package/operation/V4_Package_GetAllPackages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document_status` | path | `string` | yes | Package status filter, for example ALL or DRAFT. |
| `pageNo` | path | `number` | yes | Page number according to the division of records per page. |
| `recordPerPage` | path | `number` | yes | Number of packages to fetch per request. |
