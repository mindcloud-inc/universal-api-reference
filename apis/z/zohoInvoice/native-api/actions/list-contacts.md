# List Contacts with Zoho Invoice

Retrieves contacts from Zoho Invoice.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts`
- **Base URL:** `https://www.zohoapis.com/invoice/v3`
- **Official documentation:** [List Contacts](https://www.zoho.com/invoice/api/v3/contacts/#list-contacts)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search_text` | query | `string` | no | Search contacts by contact name or notes. Maximum length: 100. |
| `contact_name` | query | `string` | no | Search contacts by contact name. Maximum length: 100. |
| `contact_name_startswith` | query | `string` | no | Variant of contact_name. Maximum length: 100. |
| `contact_name_contains` | query | `string` | no | Variant of contact_name. Maximum length: 100. |
| `company_name` | query | `string` | no | Search contacts by company name. Maximum length: 100. |
| `company_name_startswith` | query | `string` | no | Variant of company_name. Maximum length: 100. |
| `company_name_contains` | query | `string` | no | Variant of company_name. Maximum length: 100. |
| `first_name` | query | `string` | no | Search contacts by first name of the contact person. Maximum length: 100. |
| `first_name_startswith` | query | `string` | no | Variant of first_name. Maximum length: 100. |
| `first_name_contains` | query | `string` | no | Variant of first_name. Maximum length: 100. |
| `last_name` | query | `string` | no | Search contacts by last name of the contact person. Maximum length: 100. |
| `last_name_startswith` | query | `string` | no | Variant of last_name. Maximum length: 100. |
| `last_name_contains` | query | `string` | no | Variant of last_name. Maximum length: 100. |
| `email` | query | `string` | no | Search contacts by email ID of the contact person. Maximum length: 100. |
| `phone` | query | `string` | no | Search contacts by phone number of the contact person. Maximum length: 100. |
| `phone_startswith` | query | `string` | no | Variant of phone. Maximum length: 100. |
| `phone_contains` | query | `string` | no | Variant of phone. Maximum length: 100. |
| `address` | query | `string` | no | Search contacts by any of the address fields. Maximum length: 100. |
| `address_startswith` | query | `string` | no | Variant of address. Maximum length: 100. |
| `address_contains` | query | `string` | no | Variant of address. Maximum length: 100. |
| `filter_by` | query | `list<string>` | no | Filter contacts by status. Accepted values: `Status.Active`, `Status.All`, `Status.Crm`, `Status.Duplicate`, `Status.Inactive`. |
| `zcrm_contact_id` | query | `string` | no | CRM Contact ID for the contact. |
| `zcrm_account_id` | query | `string` | no | CRM Account ID for the contact. |
