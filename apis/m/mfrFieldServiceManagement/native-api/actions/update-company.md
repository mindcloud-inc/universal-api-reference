# Update Company with mfr Field Service Management

Updates a company in mfr Field Service Management.

## Endpoint

- **Method:** `PUT`
- **Path:** `Companies({{id}}L)`
- **Base URL:** `https://portal.mobilefieldreport.com/odata`
- **Official documentation:** [Update Company](https://documenter.getpostman.com/view/6932380/2sB3dWsn6U)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | — |
| `Id` | body | `string` | yes | Record ID in the request body. |
| `Name` | body | `string` | no | Updated company name. |
| `ExternalId` | body | `string` | no | Updated external identifier. |
| `Note` | body | `string` | no | Updated company note. |
| `Location` | body | `object` | no | Company location object. |
| `IsPhysicalPerson` | body | `boolean` | no | Whether the company is a physical person. |
| `SupportTelephone` | body | `string` | no | Support phone number. |
| `SupportFax` | body | `string` | no | Support fax number. |
| `SupportMail` | body | `string` | no | Support email address. |
| `IsSupplier` | body | `boolean` | no | Whether the company is a supplier. |
| `MainContactId` | body | `string` | no | Main contact identifier. |
