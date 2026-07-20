# List Customers with Ascora

Retrieves customers from Ascora.

## Endpoint

- **Method:** `GET`
- **Path:** `/Customers/Customers`
- **Base URL:** `https://api.ascora.com.au`
- **Official documentation:** [List Customers](https://www.dropbox.com/scl/fi/75586ygs35arfb7d3cvxi/API-Endpoints-1.2.pdf?rlkey=ztci7pf4nuasegnybjreqsqe2&dl=0#page=7)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `AssignedUser` | query | `string` | no | Filter by the full name of the assigned user. |
| `CustomerType` | query | `string` | no | Filter by Ascora customer type name. |
| `FilterText` | query | `string` | no | Contains search across customer number, contact, company, email, and phone details. |
| `LeadSource` | query | `string` | no | Filter by lead source name. |
| `PhoneNumber` | query | `string` | no | Search across phone and mobile values. |
| `SiteBillingType` | query | `string` | no | Restrict results to Site, Billing, or All customers. |
| `PageSize` | query | `number` | no | Result page size. |
| `Page` | query | `number` | no | Page number to retrieve. |
