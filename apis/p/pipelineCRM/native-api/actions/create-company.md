# Create Company with Pipeline CRM

Creates a new company in Pipeline CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/companies`
- **Base URL:** `https://api.pipelinecrm.com/api/v3`
- **Official documentation:** [Create Company](https://app.pipelinecrm.com/openapi.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `check_for_duplicates` | query | `boolean` | no | Return an error when attempting to create a duplicate company. |
| `deliver_assignment_email` | query | `boolean` | no | Send an assignment email when the company is assigned to another user. |
| `company.name` | body | `string` | no | The name of the company. |
| `company.description` | body | `string` | no | Description of the company. |
| `company.email` | body | `string` | no | The company email address. |
| `company.web` | body | `string` | no | The company's website. |
| `company.phone1` | body | `string` | no | Primary business number. |
| `company.phone1_desc` | body | `string` | no | Description for the primary business number. |
| `company.owner_id` | body | `number` | no | The owner user ID of the company. |
| `company.address_1` | body | `string` | no | First line of the business address. |
| `company.address_2` | body | `string` | no | Second line of the business address. |
| `company.city` | body | `string` | no | Business address city. |
| `company.state` | body | `string` | no | Business address state. |
| `company.postal_code` | body | `string` | no | Business address postal code. |
| `company.country` | body | `string` | no | Business address country. |
| `company.tag_ids[]` | body | `array<number>` | no | Tag IDs to set on this company. |
| `todo_template_id` | body | `number` | no | The todo template ID to apply to this company. |
| `todo_template_user_id` | body | `number` | no | The owner of tasks created from the todo template. |
