# Create Company with Hubflo

Creates a new company in Hubflo.

## Endpoint

- **Method:** `POST`
- **Path:** `/companies`
- **Base URL:** `https://app.hubflo.com/api/v2`
- **Official documentation:** [Create Company](https://hubflo.readme.io/reference/post_api-v2-companies)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `address` | body | `string` | no |
| `city` | body | `string` | no |
| `country` | body | `string` | no |
| `email` | body | `string` | no |
| `hubspot_id` | body | `string` | no |
| `name` | body | `string` | yes |
| `owner_id` | body | `string` | no |
| `postal_code` | body | `string` | no |
| `siret` | body | `string` | no |
| `staff` | body | `string` | no |
| `state` | body | `string` | no |
| `url_linkedin` | body | `string` | no |
| `vat_number` | body | `string` | no |
| `website` | body | `string` | no |
| `business_description` | body | `string` | no |
| `tags` | body | `list<string>` | no |
