# Update Supplier with Ascora

Updates an existing supplier in Ascora.

## Endpoint

- **Method:** `POST`
- **Path:** `/Suppliers/Supplier`
- **Base URL:** `https://api.ascora.com.au`
- **Official documentation:** [Update Supplier](https://www.dropbox.com/scl/fi/75586ygs35arfb7d3cvxi/API-Endpoints-1.2.pdf?rlkey=ztci7pf4nuasegnybjreqsqe2&dl=0#page=67)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `businessNumber` | body | `string` | no | Business number such as ABN. |
| `emailAddress` | body | `string` | no | Email address. |
| `mobile` | body | `string` | no | Mobile number. |
| `name` | body | `string` | yes | Supplier name. |
| `notes` | body | `string` | no | Supplier notes. |
| `phone` | body | `string` | no | Phone number. |
| `streetLine1` | body | `string` | no | Street address line 1. |
| `streetPostcode` | body | `string` | no | Street postcode. |
| `streetState` | body | `string` | no | Street state. |
| `streetSuburb` | body | `string` | no | Street suburb. |
| `supplierId` | body | `string` | yes | Existing supplier ID to update. |
