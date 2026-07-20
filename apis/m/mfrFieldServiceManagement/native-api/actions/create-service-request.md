# Create Service Request with mfr Field Service Management

Creates a service request in mfr Field Service Management.

## Endpoint

- **Method:** `POST`
- **Path:** `ServiceRequests`
- **Base URL:** `https://portal.mobilefieldreport.com/odata`
- **Official documentation:** [Create Service Request](https://documenter.getpostman.com/view/6932380/2sB3dWsn6U)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Name` | body | `string` | yes | Service request name. |
| `Description` | body | `string` | no | Service request description. |
| `ExternalId` | body | `string` | no | External identifier for the service request. |
| `CustomerId` | body | `string` | no | Customer company identifier. |
| `TargetTimeInMinutes` | body | `number` | no | Planned target time in minutes. |
| `DueDateRangeEnd` | body | `date` | no | Due date range end timestamp. |
| `State` | body | `string` | no | Service request state. |
| `Type` | body | `string` | no | Service request type. |
