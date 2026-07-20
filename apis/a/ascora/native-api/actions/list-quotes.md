# List Quotes with Ascora

Retrieves quotes from Ascora.

## Endpoint

- **Method:** `GET`
- **Path:** `/Quotes/Quotes`
- **Base URL:** `https://api.ascora.com.au`
- **Official documentation:** [List Quotes](https://www.dropbox.com/scl/fi/75586ygs35arfb7d3cvxi/API-Endpoints-1.2.pdf?rlkey=ztci7pf4nuasegnybjreqsqe2&dl=0#page=25)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `AssignedUser` | query | `string` | no | Filter by the full name of the assigned user. |
| `CustomerName` | query | `string` | no | Partial match against the site or billing customer name. |
| `FilterText` | query | `string` | no | Partial match against quote number, name, or address. |
| `JobType` | query | `string` | no | Filter by related job type name. |
| `QuoteStatus` | query | `string` | no | Quote status such as IN-PROGRESS, SENT-TO-CUSTOMER, OPEN, WON, LAST-7-DAYS, ALL, or ACCEPTED. |
| `StartDate` | query | `date` | no | Filter for quotes created on or after this date. |
| `EndDate` | query | `date` | no | Filter for quotes created on or before this date. |
| `PageSize` | query | `number` | no | Result page size. Ascora defaults to 250 when omitted. |
| `Page` | query | `number` | no | Page number to retrieve. Ascora defaults to page 1 when omitted. |
