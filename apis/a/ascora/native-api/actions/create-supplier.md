# Create Supplier with Ascora

Creates a new supplier in Ascora.

## Endpoint

- **Method:** `POST`
- **Path:** `/Suppliers/Supplier`
- **Base URL:** `https://api.ascora.com.au`
- **Official documentation:** [Create Supplier](https://www.dropbox.com/scl/fi/75586ygs35arfb7d3cvxi/API-Endpoints-1.2.pdf?rlkey=ztci7pf4nuasegnybjreqsqe2&dl=0#page=67)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name of the supplier. |
| `businessNumber` | body | `string` | no | Business number for the supplier, such as an ABN. |
| `notes` | body | `string` | no | Notes associated with the supplier. |
| `phone` | body | `string` | no | Primary phone number for the supplier. |
| `mobile` | body | `string` | no | Mobile number for the supplier. |
| `emailAddress` | body | `string` | no | Email address for the supplier. |
| `streetLine1` | body | `string` | no | Street address line 1 for the supplier. |
| `streetSuburb` | body | `string` | no | Street suburb for the supplier. |
| `streetState` | body | `string` | no | Street state for the supplier. |
| `streetPostcode` | body | `string` | no | Street postcode for the supplier. |
