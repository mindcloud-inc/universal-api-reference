# Upsert Contact with Ascora

Creates or updates a contact in Ascora.

## Endpoint

- **Method:** `POST`
- **Path:** `/Customers/Contact`
- **Base URL:** `https://api.ascora.com.au`
- **Official documentation:** [Upsert Contact](https://www.dropbox.com/scl/fi/75586ygs35arfb7d3cvxi/API-Endpoints-1.2.pdf?rlkey=ztci7pf4nuasegnybjreqsqe2&dl=0#page=12)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `contactId` | body | `string` | no |
| `customerId` | body | `string` | no |
| `firstName` | body | `string` | no |
| `lastName` | body | `string` | no |
| `emailAddress` | body | `string` | no |
| `phoneNumber` | body | `string` | no |
| `mobileNumber` | body | `string` | no |
| `faxNumber` | body | `string` | no |
| `defaultContact` | body | `boolean` | no |
| `contactRole` | body | `string` | no |
