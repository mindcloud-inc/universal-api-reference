# Update Company with OnePageCRM

Updates an existing company in OnePageCRM.

## Endpoint

- **Method:** `PUT`
- **Path:** `/companies/:company_id`
- **Base URL:** `https://app.onepagecrm.com/api/v3`
- **Official documentation:** [Update Company](https://developer.onepagecrm.com/api/#/Companies/put_companies__company_id_)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_id` | path | `list<string>` | yes | ID of the company to update |
| `name` | body | `string` | no | Updated company name |
| `description` | body | `string` | no | Updated company description |
| `url` | body | `string` | no | Updated company website URL |
| `phone` | body | `string` | no | Updated company phone number |
| `address.address` | body | `string` | no | Street address for the company |
| `address.city` | body | `string` | no | City for the company address |
| `address.state` | body | `string` | no | State for the company address |
| `address.zip_code` | body | `string` | no | ZIP code for the company address |
| `address.country_code` | body | `string` | no | ISO-3166 country code for the company address |
| `company_fields[].company_field.id` | body | `string` | no | ID of the company custom field to update |
| `company_fields[].value` | body | `string` | no | Value for the company custom field |
