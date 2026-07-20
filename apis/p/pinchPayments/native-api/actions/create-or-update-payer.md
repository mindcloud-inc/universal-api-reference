# Create or Update Payer with Pinch Payments

Creates or updates a payer in Pinch Payments.

## Endpoint

- **Method:** `POST`
- **Path:** `/payers`
- **Base URL:** `https://api.getpinch.com.au/live`
- **Official documentation:** [Create or Update Payer](https://docs.getpinch.com.au/reference/save-payer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyName` | body | `string` | no | Company name for the payer. |
| `companyRegistrationNumber` | body | `string` | no | Company registration number for the payer. |
| `country` | body | `string` | no | Country for the payer. |
| `emailAddress` | body | `string` | yes | Email address for the payer. |
| `firstName` | body | `string` | yes | First name for the payer. |
| `fullName` | body | `string` | no | Full name for the payer. |
| `id` | body | `string` | no | If you include an ID this endpoint updates an existing payer; otherwise it creates a new payer. |
| `lastName` | body | `string` | no | Last name for the payer. |
| `metadata` | body | `string` | no | Additional metadata for the payer. |
| `mobileNumber` | body | `string` | no | Mobile number for the payer. |
| `postcode` | body | `string` | no | Postcode for the payer. |
| `source.ipAddress` | body | `string` | no | IP address associated with the payment source. |
| `source.sourceType` | body | `string` | no | Currently either bank-account or credit-card when creating a payment source with the payer. |
| `source.token` | body | `string` | no | Token created by the capture script when adding a payment source with the payer. |
| `state` | body | `string` | no | State for the payer. |
| `streetAddress` | body | `string` | no | Street address for the payer. |
| `suburb` | body | `string` | no | Suburb for the payer. |
