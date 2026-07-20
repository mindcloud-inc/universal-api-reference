# Add E-commerce Store with Mailchimp

Creates a new e-commerce store in Mailchimp.

## Endpoint

- **Method:** `POST`
- **Path:** `ecommerce/stores`
- **Base URL:** `https://{serverPrefix}.api.mailchimp.com/3.0/`
- **Official documentation:** [Add E-commerce Store](https://us22.api.mailchimp.com/schema/3.0/Paths/Ecommerce/Stores/Collection.json)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | body | `string` | yes |
| `list_id` | body | `list` | yes |
| `name` | body | `string` | yes |
| `currency_code` | body | `string` | yes |
| `platform` | body | `string` | no |
| `domain` | body | `string` | no |
| `is_syncing` | body | `boolean` | no |
| `email_address` | body | `string` | no |
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
