# Find Service Request by ID with mfr Field Service Management

Finds a service request in mfr Field Service Management by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `ServiceRequests?$filter=Id eq {{id}}L`
- **Base URL:** `https://portal.mobilefieldreport.com/odata`
- **Official documentation:** [Find Service Request by ID](https://documenter.getpostman.com/view/6932380/2sB3dWsn6U)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `number` | yes |
