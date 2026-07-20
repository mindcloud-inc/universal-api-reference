# Update Service Request with mfr Field Service Management

Updates a service request in mfr Field Service Management.

## Endpoint

- **Method:** `PUT`
- **Path:** `ServiceRequests({{id}}L)`
- **Base URL:** `https://portal.mobilefieldreport.com/odata`
- **Official documentation:** [Update Service Request](https://documenter.getpostman.com/view/6932380/2sB3dWsn6U)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | — |
| `Id` | body | `string` | yes | Record ID in the request body. |
| `Name` | body | `string` | no | Updated service request name. |
| `ExternalId` | body | `string` | no | Updated external identifier. |
| `CustomerId` | body | `string` | no | Customer company ID for the service request. |
| `Description` | body | `string` | no | Updated service request description. |
| `State` | body | `string` | no | Updated service request state. |
| `Type` | body | `string` | no | Updated service request type. |
| `TargetTimeInMinutes` | body | `number` | no | Updated target duration in minutes. |
