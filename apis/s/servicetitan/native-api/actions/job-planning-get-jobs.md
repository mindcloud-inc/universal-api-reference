# Get Jobs with ServiceTitan

## Endpoint

- **Method:** `GET`
- **Path:** `https://api.servicetitan.io/jpm/v2/tenant/{tenant}/jobs`
- **Base URL:** `https://{baseUrl}/`
- **Official documentation:** [Get Jobs](https://developer.servicetitan.io/api-details/#api=tenant-jpm-v2&operation=Jobs_GetList)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bookingId` | query | `number` | no | Filters by booking ID that resulted in this job |
| `projectId` | query | `number` | no | Filters by project ID |
| `locationId` | query | `number` | no | Filters by job's location ID |
| `customerId` | query | `number` | no | Filters by job's customer ID |
| `ids` | query | `string` | no | — |
| `number` | query | `string` | no | — |
| `firstAppointmentStartsOnOrAfter` | query | `string` | no | — |
| `firstAppointmentStartsBefore` | query | `string` | no | — |
| `appointmentStartsOnOrAfter` | query | `string` | no | — |
| `appointmentStartsBefore` | query | `string` | no | — |
| `createdBefore` | query | `string` | no | — |
| `createdOnOrAfter` | query | `string` | no | — |
| `modifiedBefore` | query | `string` | no | — |
| `modifiedOnOrAfter` | query | `string` | no | — |
| `completedOnOrAfter` | query | `string` | no | — |
| `completedBefore` | query | `string` | no | — |
| `sort` | query | `string` | no | — |
| `externalDataApplicationGuid` | query | `string` | no | — |
| `externalDataKey` | query | `string` | no | — |
| `externalDataValues` | query | `string` | no | — |
| `jobStatus` | query | `list<string>` | no | Filters by job status Values: [Scheduled, Dispatched, InProgress, Hold, Completed, Canceled] |
| `appointmentStatus` | query | `string` | no | — |
| `priority` | query | `string` | no | — |
| `technicianId` | query | `number` | no | — |
| `soldById` | query | `number` | no | — |
| `jobTypeId` | query | `number` | no | — |
| `campaignId` | query | `number` | no | — |
| `businessUnitId` | query | `number` | no | — |
| `invoiceId` | query | `number` | no | — |
| `tagTypeIds` | query | `string` | no | — |
| `hasUnusedAppointments` | query | `boolean` | no | — |
