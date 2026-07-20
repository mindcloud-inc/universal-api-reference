# Create Proposal with Hubflo

Creates a draft proposal in Hubflo.

## Endpoint

- **Method:** `POST`
- **Path:** `/proposals`
- **Base URL:** `https://app.hubflo.com/api/v2`
- **Official documentation:** [Create Proposal](https://hubflo.readme.io/reference/post_api-v2-proposals)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `title` | body | `string` | yes |
| `description` | body | `string` | no |
| `quote_comment` | body | `string` | no |
| `user_id` | body | `string` | yes |
| `project_id` | body | `string` | no |
| `expires_in_days` | body | `number` | no |
| `payment_terms` | body | `string` | no |
| `contact_ids` | body | `list<string>` | no |
| `payment_methods` | body | `list<string>` | no |
