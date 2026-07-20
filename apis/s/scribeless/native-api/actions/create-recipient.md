# Create Recipient with Scribeless

## Endpoint

- **Method:** `POST`
- **Path:** `/api/recipients`
- **Base URL:** `https://platform.scribeless.co`
- **Official documentation:** [Create Recipient](https://docs.scribeless.co/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | body | `string` | yes | The Scribeless campaign ID that will receive the recipient. |
| `data` | body | `object` | yes | Recipient payload object for a single Scribeless recipient. |
| `title` | body | `string` | no | Recipient title such as Mr or Mrs. |
| `firstName` | body | `string` | no | Recipient first name. |
| `lastName` | body | `string` | no | Recipient last name. |
| `company` | body | `string` | no | Recipient company name. |
| `address` | body | `object` | no | Recipient mailing address object. |
| `address1` | body | `string` | no | First line of the mailing address. |
| `address2` | body | `string` | no | Second line of the mailing address. |
| `address3` | body | `string` | no | Third line of the mailing address. |
| `city` | body | `string` | no | City for the mailing address. |
| `state` | body | `string` | no | State, county, or region for the mailing address. |
| `postalCode` | body | `string` | no | Postal or ZIP code for the mailing address. |
| `country` | body | `string` | no | Two-letter country code for the mailing address. |
| `variables` | body | `object` | no | Custom variable values for Scribeless merge fields. |
| `custom1` | body | `string` | no | Value for the custom1 merge field. |
| `custom2` | body | `string` | no | Value for the custom2 merge field. |
