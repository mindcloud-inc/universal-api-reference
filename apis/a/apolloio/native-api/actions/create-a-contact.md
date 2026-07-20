# Create a Contact with Apollo

Creates a new contact in Apollo.

## Endpoint

- **Method:** `POST`
- **Path:** `v1/contacts`
- **Base URL:** `https://app.apollo.io/api`
- **Official documentation:** [Create a Contact](https://docs.apollo.io/reference/create-a-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `first_name` | body | `string` | no | The first name of the contact you want to create. Example: `Tim` |
| `last_name` | body | `string` | no | The last name of the contact you want to create. Example: `Zheng` |
| `organization_name` | body | `string` | no | The name of the contact's employer (company). Example: `apollo` |
| `title` | body | `string` | no | The current job title that the contact holds. Example: `senior research analyst` |
| `account_id` | body | `string` | no | The Apollo ID for the account. Example: `63f53afe4ceeca00016bdd2f` |
| `email` | body | `string` | no | The email address of the contact. Example: `example@email.com` |
| `website_url` | body | `string` | no | The corporate website URL. Example: `https://www.apollo.io/` |
| `label_names[]` | body | `array<string>` | no | Lists to which the contact belongs. |
| `contact_stage_id` | body | `string` | no | The Apollo ID for the contact stage. Example: `6095a710bd01d100a506d4ae` |
| `present_raw_address` | body | `string` | no | The personal location for the contact. Example: `Atlanta, United States` |
| `direct_phone` | body | `string` | no | The primary phone number. Example: `555-303-1234` |
| `corporate_phone` | body | `string` | no | The work/office phone number. Example: `+44 7911 123456` |
| `mobile_phone` | body | `string` | no | The mobile phone number. Example: `555-303-1234` |
| `home_phone` | body | `string` | no | The home phone number. Example: `555-303-1234` |
| `other_phone` | body | `string` | no | Alternative phone number. Example: `555-303-1234` |
| `typed_custom_fields` | body | `object` | no | Add information to custom fields in Apollo. Your custom fields are unique to your team's Apollo account. This means that the examples in this documentation may not work for your testing purposes. To utilize this parameter successfully, call the Get a List of All Custom Fields endpoint and identify the `id` value for the custom field, as well as the appropriate data type. For example, if a custom field accepts picklist entries, you need to pass the accompanying `id` value for the picklist entry that you want to use as the input value. Example : When the Get a List of All Custom Fields endpoint returns an `id` of field: * `"60c39ed82bd02f01154c470a"` (datetime) then the value passed should be: `{"60c39ed82bd02f01154c470a": "2025-08-07"}` |
| `run_dedupe` | body | `boolean` | no | Set to `true` to enable deduplication logic that prevents creating duplicate contacts. When enabled, Apollo will check for existing contacts with matching email addresses, names, or other identifying information and return the existing contact instead of creating a duplicate. The default value is `false`. When deduplication is enabled, performance may be slightly impacted due to the additional validation checks, but this ensures data integrity and prevents duplicate entries in your database. |
