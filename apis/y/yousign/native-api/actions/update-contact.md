# Update Contact with Yousign

Updates an existing contact in Yousign.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/contacts/:contactId`
- **Base URL:** `https://api-sandbox.yousign.app/v3`
- **Official documentation:** [Update Contact](https://developers.yousign.com/reference/patch-contacts-contactid-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactId` | path | `string` | yes | The Yousign contact ID. |
| `first_name` | body | `string` | no | Updated contact first name. |
| `last_name` | body | `string` | no | Updated contact last name. |
| `email` | body | `string` | no | Updated contact email address. |
| `locale` | body | `string` | no | Updated contact locale. |
| `phone_number` | body | `string` | no | Updated contact phone number in E.164 format. |
| `company_name` | body | `string` | no | Updated contact company name. |
| `job_title` | body | `string` | no | Updated contact job title. |
| `workspace_id` | body | `string` | no | Updated contact workspace ID. |
| `address_line_1` | body | `string` | no | Updated contact address line 1. |
| `address_line_2` | body | `string` | no | Updated contact address line 2. |
| `address_city` | body | `string` | no | Updated contact address city. |
| `address_postal_code` | body | `string` | no | Updated contact address postal code. |
| `address_country` | body | `string` | no | Updated contact address country. |
