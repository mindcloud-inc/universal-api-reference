# Update Contact with Hubflo

Updates an existing contact in Hubflo.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/contacts/:id`
- **Base URL:** `https://app.hubflo.com/api/v2`
- **Official documentation:** [Update Contact](https://hubflo.readme.io/reference/patch_api-v2-contacts-id)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `address` | body | `string` | no |
| `city` | body | `string` | no |
| `company_id` | body | `string` | no |
| `company_name` | body | `string` | no |
| `contact_type` | body | `string` | no |
| `country` | body | `string` | no |
| `email` | body | `string` | no |
| `full_name` | body | `string` | no |
| `hubspot_id` | body | `string` | no |
| `id` | path | `string` | yes |
| `job_title` | body | `string` | no |
| `owner_email` | body | `string` | no |
| `owner_id` | body | `string` | no |
| `phone` | body | `string` | no |
| `postal_code` | body | `string` | no |
| `priority` | body | `string` | no |
| `secondary_phone` | body | `string` | no |
| `state` | body | `string` | no |
| `url_linkedin` | body | `string` | no |
| `first_name` | body | `string` | yes |
| `last_name` | body | `string` | yes |
| `tags` | body | `list<string>` | no |
