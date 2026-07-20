# Update Service Object with mfr Field Service Management

Updates a service object in mfr Field Service Management.

## Endpoint

- **Method:** `PUT`
- **Path:** `ServiceObjects({{id}}L)`
- **Base URL:** `https://portal.mobilefieldreport.com/odata`
- **Official documentation:** [Update Service Object](https://documenter.getpostman.com/view/6932380/2sB3dWsn6U)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | — |
| `Id` | body | `string` | yes | Record ID in the request body. |
| `Name` | body | `string` | no | Updated service object name. |
| `Note` | body | `string` | no | Updated service object note. |
| `ExternalId` | body | `string` | no | Updated external identifier. |
| `CompanyId` | body | `string` | no | Updated company ID. |
