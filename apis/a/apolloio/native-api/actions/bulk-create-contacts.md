# Bulk Create Contacts with Apollo

Creates multiple new contacts in Apollo.

## Endpoint

- **Method:** `POST`
- **Path:** `v1/contacts/bulk_create`
- **Base URL:** `https://app.apollo.io/api`
- **Official documentation:** [Bulk Create Contacts](https://docs.apollo.io/reference/bulk-create-contacts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contacts[]` | body | `array<object>` | yes | Array of contact objects to create (maximum 100 contacts per request) |
| `contacts[].first_name` | body | `string` | no | Contact's first name |
| `contacts[].last_name` | body | `string` | no | Contact's last name |
| `contacts[].email` | body | `string` | no | Contact's email address |
| `contacts[].title` | body | `string` | no | Contact's job title |
| `contacts[].primary_title` | body | `string` | no | Primary job title (takes precedence over title) |
| `contacts[].organization_name` | body | `string` | no | Company/organization name |
| `contacts[].phone` | body | `string` | no | Phone number |
| `contacts[].present_raw_address` | body | `string` | no | Physical address |
| `contacts[].linkedin_url` | body | `string` | no | LinkedIn profile URL |
| `contacts[].facebook_url` | body | `string` | no | Facebook profile URL |
| `contacts[].twitter_url` | body | `string` | no | Twitter profile URL |
| `contacts[].photo_url` | body | `string` | no | Profile photo URL |
| `contacts[].account_id` | body | `string` | no | Associated account ID |
| `contacts[].organization_id` | body | `string` | no | Associated organization ID |
| `contacts[].owner_id` | body | `string` | no | Contact owner user ID (defaults to current user if not provided) |
| `contacts[].contact_stage_id` | body | `string` | no | Contact stage ID |
| `contacts[].salesforce_id` | body | `string` | no | Salesforce ID for matching and deduplication |
| `contacts[].hubspot_id` | body | `string` | no | HubSpot ID for matching and deduplication |
| `contacts[].salesforce_lead_id` | body | `string` | no | Salesforce Lead ID |
| `contacts[].salesforce_contact_id` | body | `string` | no | Salesforce Contact ID for matching |
| `contacts[].salesforce_account_id` | body | `string` | no | Salesforce Account ID |
| `contacts[].outreach_id` | body | `string` | no | Outreach.io ID |
| `contacts[].salesloft_id` | body | `string` | no | SalesLoft ID |
| `contacts[].phone_status_cd` | body | `string` | no | Phone validation status |
| `contacts[].typed_custom_fields` | body | `object` | no | Custom field values as key-value pairs where key is the field_id and value is the field_value |
| `contacts[].contact_emails[]` | body | `array<object>` | no | Array of email objects with position |
| `contacts[].contact_emails[].email` | body | `string` | no | — |
| `contacts[].contact_emails[].position` | body | `number` | no | — |
| `contacts[].phone_numbers[]` | body | `array<object>` | no | Array of phone number objects |
| `contacts[].phone_numbers[].raw_number` | body | `string` | no | — |
| `contacts[].phone_numbers[].position` | body | `number` | no | — |
| `contacts[].contact_role_type_ids[]` | body | `array<string>` | no | Array of contact role type IDs |
| `contacts[].append_label_names[]` | body | `array<string>` | no | Array of label names to add to the contact |
| `run_dedupe` | body | `boolean` | no | Enable full deduplication across all sources. When false (default), creates duplicates for non-email_import sources and merges with email_import placeholders only. When true, returns existing contacts without modifying them (except email_import placeholders which are still merged). Matches by email, CRM IDs, or name + organization |
