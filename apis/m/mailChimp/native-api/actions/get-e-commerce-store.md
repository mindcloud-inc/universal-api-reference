# Get E-commerce Store with Mailchimp

Retrieves an e-commerce store from Mailchimp.

## Endpoint

- **Method:** `GET`
- **Path:** `ecommerce/stores/:store_id`
- **Base URL:** `https://{serverPrefix}.api.mailchimp.com/3.0/`
- **Official documentation:** [Get E-commerce Store](https://us22.api.mailchimp.com/schema/3.0/Paths/Ecommerce/Stores/Instance.json)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `store_id` | path | `string` | yes |
| `fields` | query | `string` | no |
| `exclude_fields` | query | `string` | no |
