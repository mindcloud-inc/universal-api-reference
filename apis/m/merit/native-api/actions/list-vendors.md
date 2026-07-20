# List Vendors with Merit

## Endpoint

- **Method:** `POST`
- **Path:** `v1/getvendors`
- **Base URL:** `https://aktiva.merit.ee/api`
- **Official documentation:** [List Vendors](https://api.merit.ee/connecting-robots/reference-manual/vendors/get-vendor-list/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Id` | body | `string` | no | Vendor GUID. If provided, other selectors are ignored. |
| `Name` | body | `string` | no | Broad vendor name match. |
| `RegNo` | body | `string` | no | Exact vendor registration number match. |
| `VatRegNo` | body | `string` | no | Exact vendor VAT registration number match. |
| `ChangedDate` | body | `string` | no | Date of changed or created vendor in YYYYmmDD format. |
| `WithComments` | body | `boolean` | no | Whether to include comments. |
| `CommentsFrom` | body | `date` | no | Only comments later than this date. |
