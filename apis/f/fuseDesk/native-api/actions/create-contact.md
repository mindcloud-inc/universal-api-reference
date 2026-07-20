# Create Contact with FuseDesk

Creates a new contact in FuseDesk.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/contacts`
- **Base URL:** `https://{appName}.fusedesk.com`
- **Official documentation:** [Create Contact](https://documenter.getpostman.com/view/11014835/SztBc8ix#39b23fd9-d985-4daa-bc3e-ba60e20eee95)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cityBilling` | body | `string` | no | Billing city. |
| `company` | body | `string` | no | Company name. |
| `countryBilling` | body | `string` | no | Billing country. |
| `emailAddress` | body | `string` | no | Primary email address. |
| `emailAddress2` | body | `string` | no | Secondary email address. |
| `emailAddress3` | body | `string` | no | Tertiary email address. |
| `firstName` | body | `string` | no | Contact first name. |
| `lastName` | body | `string` | no | Contact last name. |
| `phone1` | body | `string` | no | Primary phone number. |
| `phone2` | body | `string` | no | Secondary phone number. |
| `phoneExt1` | body | `string` | no | Primary phone extension. |
| `phoneExt2` | body | `string` | no | Secondary phone extension. |
| `postalBilling` | body | `string` | no | Billing postal code. |
| `stateBilling` | body | `string` | no | Billing state or region. |
| `street1Billing` | body | `string` | no | Billing street address line 1. |
| `street2Billing` | body | `string` | no | Billing street address line 2. |
| `timeZone` | body | `string` | no | Time zone identifier. |
| `website` | body | `string` | no | Website URL. |
