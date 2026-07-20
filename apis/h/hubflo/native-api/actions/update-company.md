# Update Company with Hubflo

Updates an existing company in Hubflo.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/companies/:id`
- **Base URL:** `https://app.hubflo.com/api/v2`
- **Official documentation:** [Update Company](https://hubflo.readme.io/reference/patch_api-v2-companies-id)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `address` | body | `string` | no |
| `city` | body | `string` | no |
| `country` | body | `string` | no |
| `email` | body | `string` | no |
| `hubspot_id` | body | `string` | no |
| `id` | path | `string` | yes |
| `owner_id` | body | `string` | no |
| `postal_code` | body | `string` | no |
| `siret` | body | `string` | no |
| `staff` | body | `string` | no |
| `state` | body | `string` | no |
| `url_linkedin` | body | `string` | no |
| `vat_number` | body | `string` | no |
| `website` | body | `string` | no |
| `name` | body | `string` | yes |
| `business_description` | body | `string` | no |
| `tags` | body | `list<string>` | no |
