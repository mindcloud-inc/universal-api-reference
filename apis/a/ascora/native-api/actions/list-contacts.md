# List Contacts with Ascora

Retrieves contacts from Ascora.

## Endpoint

- **Method:** `GET`
- **Path:** `/Customers/Contacts`
- **Base URL:** `https://api.ascora.com.au`
- **Official documentation:** [List Contacts](https://www.dropbox.com/scl/fi/75586ygs35arfb7d3cvxi/API-Endpoints-1.2.pdf?rlkey=ztci7pf4nuasegnybjreqsqe2&dl=0#page=10)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `FilterText` | query | `string` | no | Contains search across contact details. |
| `PhoneNumber` | query | `string` | no | Exact match across phone and mobile after removing spaces. |
| `PageSize` | query | `number` | no | Result page size. |
| `Page` | query | `number` | no | Page number to retrieve. |
