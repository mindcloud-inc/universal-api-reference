# Create Company with mfr Field Service Management

Creates a company in mfr Field Service Management.

## Endpoint

- **Method:** `POST`
- **Path:** `Companies`
- **Base URL:** `https://portal.mobilefieldreport.com/odata`
- **Official documentation:** [Create Company](https://documenter.getpostman.com/view/6932380/2sB3dWsn6U)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Name` | body | `string` | yes | Company name. |
| `ExternalId` | body | `string` | no | External identifier for the company. |
| `IsPhysicalPerson` | body | `boolean` | no | Whether the company is a physical person. |
| `Location` | body | `object` | no | Company location object. |
| `Note` | body | `string` | no | Company note. |
| `SupportTelephone` | body | `string` | no | Support telephone number. |
| `SupportFax` | body | `string` | no | Support fax number. |
| `SupportMail` | body | `string` | no | Support email address. |
| `IsSupplier` | body | `boolean` | no | Whether the company is a supplier. |
| `MainContactId` | body | `string` | no | Main contact ID for the company. |
