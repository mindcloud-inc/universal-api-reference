# Create Enquiry with Ascora

Creates a new enquiry in Ascora.

## Endpoint

- **Method:** `POST`
- **Path:** `/Enquiry`
- **Base URL:** `https://api.ascora.com.au`
- **Official documentation:** [Create Enquiry](https://www.dropbox.com/scl/fi/75586ygs35arfb7d3cvxi/API-Endpoints-1.2.pdf?rlkey=ztci7pf4nuasegnybjreqsqe2&dl=0#page=4)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `companyName` | body | `string` | no |
| `firstName` | body | `string` | no |
| `lastName` | body | `string` | no |
| `email` | body | `string` | no |
| `mobile` | body | `string` | no |
| `phone` | body | `string` | no |
| `addressLine1` | body | `string` | no |
| `addressLine2` | body | `string` | no |
| `addressSuburb` | body | `string` | no |
| `addressState` | body | `string` | no |
| `addressPostcode` | body | `string` | no |
| `addressCountry` | body | `string` | no |
| `enquiryDescription` | body | `string` | no |
| `leadSource` | body | `string` | no |
