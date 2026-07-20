# List Service Requests by External ID with mfr Field Service Management

Finds service requests in mfr Field Service Management by external ID.

## Endpoint

- **Method:** `GET`
- **Path:** `ServiceRequests?$filter=ExternalId eq '{{externalId}}'`
- **Base URL:** `https://portal.mobilefieldreport.com/odata`
- **Official documentation:** [List Service Requests by External ID](https://documenter.getpostman.com/view/6932380/2sB3dWsn6U)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `externalId` | path | `string` | yes |
