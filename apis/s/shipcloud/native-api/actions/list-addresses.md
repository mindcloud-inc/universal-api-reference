# List Addresses with Shipcloud

Retrieves addresses from Shipcloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/addresses`
- **Base URL:** `https://api.shipcloud.io/v1`
- **Official documentation:** [List Addresses](https://developers.shipcloud.io/swagger-ui/#/default/get_addresses)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `care_of` | query | `string` | no | Filter addresses by care-of value. |
| `city` | query | `string` | no | Filter addresses by city. |
| `company` | query | `string` | no | Filter addresses by company name. |
| `country` | query | `string` | no | Filter addresses by ISO country code. |
| `first_name` | query | `string` | no | Filter addresses by first name. |
| `last_name` | query | `string` | no | Filter addresses by last name. |
| `page` | query | `number` | no | Page number for paginated address results. |
| `per_page` | query | `number` | no | Number of address records to return per page. |
| `phone` | query | `string` | no | Filter addresses by phone number. |
| `street` | query | `string` | no | Filter addresses by street name. |
| `street_no` | query | `string` | no | Filter addresses by street number. |
| `zip_code` | query | `string` | no | Filter addresses by ZIP or postal code. |
