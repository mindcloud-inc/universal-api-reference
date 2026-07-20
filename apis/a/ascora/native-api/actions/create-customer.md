# Create Customer with Ascora

Creates a new customer in Ascora.

## Endpoint

- **Method:** `POST`
- **Path:** `/Customers/Customer`
- **Base URL:** `https://api.ascora.com.au`
- **Official documentation:** [Create Customer](https://www.dropbox.com/scl/fi/75586ygs35arfb7d3cvxi/API-Endpoints-1.2.pdf?rlkey=ztci7pf4nuasegnybjreqsqe2&dl=0#page=13)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `companyName` | body | `string` | no |
| `contactFirstName` | body | `string` | no |
| `contactLastName` | body | `string` | no |
| `emailAddress` | body | `string` | no |
| `phoneNumber` | body | `string` | no |
| `mobileNumber` | body | `string` | no |
| `onHold` | body | `boolean` | no |
| `billingCustomerOnHold` | body | `boolean` | no |
| `streetLine1` | body | `string` | no |
| `streetLine2` | body | `string` | no |
| `streetSuburb` | body | `string` | no |
| `streetPostcode` | body | `string` | no |
| `streetState` | body | `string` | no |
| `streetCountry` | body | `string` | no |
| `customerType.name` | body | `string` | no |
| `leadSource.name` | body | `string` | no |
