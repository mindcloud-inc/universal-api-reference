# List Service Objects by Company with mfr Field Service Management

Finds service objects in mfr Field Service Management by company.

## Endpoint

- **Method:** `GET`
- **Path:** `ServiceObjects?$filter=Company/Id eq {{companyId}}L`
- **Base URL:** `https://portal.mobilefieldreport.com/odata`
- **Official documentation:** [List Service Objects by Company](https://documenter.getpostman.com/view/6932380/2sB3dWsn6U)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `companyId` | path | `number` | yes |
