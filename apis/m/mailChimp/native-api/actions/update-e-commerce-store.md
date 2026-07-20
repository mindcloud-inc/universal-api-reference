# Update E-commerce Store with Mailchimp

Updates an existing e-commerce store in Mailchimp.

## Endpoint

- **Method:** `PATCH`
- **Path:** `ecommerce/stores/:store_id`
- **Base URL:** `https://{serverPrefix}.api.mailchimp.com/3.0/`
- **Official documentation:** [Update E-commerce Store](https://us22.api.mailchimp.com/schema/3.0/Paths/Ecommerce/Stores/Instance.json)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `store_id` | path | `string` | yes |
| `name` | body | `string` | no |
| `platform` | body | `string` | no |
| `domain` | body | `string` | no |
| `is_syncing` | body | `boolean` | no |
| `email_address` | body | `string` | no |
| `currency_code` | body | `string` | no |
| `money_format` | body | `string` | no |
| `primary_locale` | body | `string` | no |
| `timezone` | body | `string` | no |
| `phone` | body | `string` | no |
| `address` | body | `object` | no |
| `address.address1` | body | `string` | no |
| `address.address2` | body | `string` | no |
| `address.city` | body | `string` | no |
| `address.province` | body | `string` | no |
| `address.province_code` | body | `string` | no |
| `address.postal_code` | body | `string` | no |
| `address.country` | body | `string` | no |
| `address.country_code` | body | `string` | no |
| `address.longitude` | body | `number` | no |
| `address.latitude` | body | `number` | no |
