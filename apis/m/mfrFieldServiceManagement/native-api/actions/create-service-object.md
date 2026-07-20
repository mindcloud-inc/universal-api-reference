# Create Service Object with mfr Field Service Management

Creates a service object in mfr Field Service Management.

## Endpoint

- **Method:** `POST`
- **Path:** `ServiceObjects`
- **Base URL:** `https://portal.mobilefieldreport.com/odata`
- **Official documentation:** [Create Service Object](https://documenter.getpostman.com/view/6932380/2sB3dWsn6U)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Name` | body | `string` | yes | Service object name. |
| `ExternalId` | body | `string` | no | External identifier for the service object. |
| `CompanyId` | body | `string` | no | Company ID linked to the service object. |
| `Location` | body | `object` | no | Service object location object. |
| `Contacts[]` | body | `array<object>` | no | Contact list for the service object. |
