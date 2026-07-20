# Get Appointments with ServiceTitan

## Endpoint

- **Method:** `GET`
- **Path:** `https://api.servicetitan.io/jpm/v2/tenant/{tenant}/appointments/`
- **Base URL:** `https://{baseUrl}/`
- **Official documentation:** [Get Appointments](https://developer.servicetitan.io/api-details/#api=tenant-jpm-v2&operation=Appointments_GetList)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `createdBefore` | query | `string` | no |
| `createdOnOrAfter` | query | `string` | no |
| `customerId` | query | `number` | no |
| `includeTotal` | query | `boolean` | no |
| `jobId` | query | `number` | no |
| `modifiedBefore` | query | `string` | no |
| `modifiedOnOrAfter` | query | `string` | no |
| `number` | query | `string` | no |
| `projectId` | query | `number` | no |
| `sort` | query | `string` | no |
| `startsBefore` | query | `string` | no |
| `startsOnOrAfter` | query | `string` | no |
| `status` | query | `string` | no |
| `technicianId` | query | `number` | no |
| `unused` | query | `boolean` | no |
