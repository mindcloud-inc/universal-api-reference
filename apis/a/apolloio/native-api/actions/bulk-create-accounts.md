# Bulk Create Accounts with Apollo

Creates multiple new accounts in Apollo.

## Endpoint

- **Method:** `POST`
- **Path:** `v1/accounts/bulk_create`
- **Base URL:** `https://app.apollo.io/api`
- **Official documentation:** [Bulk Create Accounts](https://docs.apollo.io/reference/bulk-create-accounts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accounts[]` | body | `array<object>` | yes | Array of account attribute objects (maximum 100 accounts per request) |
| `accounts[].name` | body | `string` | no | Account name |
| `accounts[].domain` | body | `string` | no | Company domain (e.g., 'example.com') |
| `accounts[].owner_id` | body | `string` | no | Account owner user ID (BSON::ObjectId format). Defaults to current user if not provided |
| `accounts[].phone` | body | `string` | no | Company phone number |
| `accounts[].phone_status_cd` | body | `string` | no | Phone validation status |
| `accounts[].raw_address` | body | `string` | no | Company address |
| `accounts[].linkedin_url` | body | `string` | no | LinkedIn company page URL |
| `accounts[].facebook_url` | body | `string` | no | Facebook page URL |
| `accounts[].twitter_url` | body | `string` | no | Twitter profile URL |
| `accounts[].salesforce_id` | body | `string` | no | Salesforce account ID for CRM integration |
| `accounts[].hubspot_id` | body | `string` | no | HubSpot company ID for CRM integration |
| `accounts[].merged_crm_ids[]` | body | `array<string>` | no | Additional CRM IDs for deduplication |
| `accounts[].organization_id` | body | `string` | no | Apollo organization ID |
| `accounts[].parent_account_id` | body | `string` | no | Parent account ID for account hierarchy (BSON::ObjectId format) |
| `accounts[].account_stage_id` | body | `string` | no | Account stage/pipeline stage ID (BSON::ObjectId format) |
| `accounts[].typed_custom_fields` | body | `object` | no | Custom field values as key-value pairs where key is the field_id and value is the field_value |
| `accounts[].append_label_names[]` | body | `array<string>` | no | Label names to apply to the account |
| `run_dedupe` | body | `boolean` | no | Enable aggressive deduplication by domain, organization_id, and name. When false (default), only matches by CRM IDs. When true, also matches by domain, organization_id, and name. Existing accounts are returned without modification in both modes |
