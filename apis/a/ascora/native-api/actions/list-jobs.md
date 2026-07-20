# List Jobs with Ascora

Retrieves jobs from Ascora.

## Endpoint

- **Method:** `GET`
- **Path:** `/Jobs/Jobs`
- **Base URL:** `https://api.ascora.com.au`
- **Official documentation:** [List Jobs](https://www.dropbox.com/scl/fi/75586ygs35arfb7d3cvxi/API-Endpoints-1.2.pdf?rlkey=ztci7pf4nuasegnybjreqsqe2&dl=0#page=52)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `AssignedUser` | query | `string` | no | Find all Jobs based on the full name of the Assigned User. |
| `CustomerName` | query | `string` | no | Find all Jobs with a partially matching Site or Billing Customer Name. |
| `EndDate` | query | `date` | no | Search for Jobs created on or before the specified date. |
| `FilterText` | query | `string` | no | Performs a partial search against the full Quote Number, Name or Address. |
| `JobStatus` | query | `string` | no | Filters the Jobs to the specified status. |
| `JobType` | query | `string` | no | Matches against the related Job Type. |
| `StartDate` | query | `date` | no | Search for Jobs created on or after the specified date. |
