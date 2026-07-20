# Find Service Object by ID with mfr Field Service Management

Finds a service object in mfr Field Service Management by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `ServiceObjects?$filter=Id eq {{id}}L`
- **Base URL:** `https://portal.mobilefieldreport.com/odata`
- **Official documentation:** [Find Service Object by ID](https://documenter.getpostman.com/view/6932380/2sB3dWsn6U)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `number` | yes |
