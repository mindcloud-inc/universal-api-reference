# Create Contact with Hubflo

Creates a new contact in Hubflo.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts`
- **Base URL:** `https://app.hubflo.com/api/v2`
- **Official documentation:** [Create Contact](https://hubflo.readme.io/reference/post_api-v2-contacts)

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
| `first_name` | body | `string` | yes |
| `full_name` | body | `string` | no |
| `hubspot_id` | body | `string` | no |
| `job_title` | body | `string` | no |
| `owner_email` | body | `string` | no |
| `owner_id` | body | `string` | no |
| `phone` | body | `string` | no |
| `postal_code` | body | `string` | no |
| `priority` | body | `string` | no |
| `secondary_phone` | body | `string` | no |
| `state` | body | `string` | no |
| `url_linkedin` | body | `string` | no |
| `last_name` | body | `string` | yes |
| `tags` | body | `list<string>` | no |
