# Update a Contact with Apollo

Updates an existing contact in Apollo.

## Endpoint

- **Method:** `PATCH`
- **Path:** `v1/contacts/:contact_id`
- **Base URL:** `https://app.apollo.io/api`
- **Official documentation:** [Update a Contact](https://docs.apollo.io/reference/update-a-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | path | `string` | yes | The Apollo ID for the contact that you want to update. To find contact IDs, call the Search for Contacts endpoint and identify the `id` value for the contact. Example: `66e34b81740c50074e3d1bd4` |
| `first_name` | body | `string` | no | Update the contact's first name. Example: `Tim` |
| `last_name` | body | `string` | no | Update the contact's last name. Example: `Zheng` |
| `organization_name` | body | `string` | no | Update the employer (company) name. Example: `apollo` |
| `title` | body | `string` | no | Update the job title. Example: `senior research analyst` |
| `account_id` | body | `string` | no | Update the account ID. Example: `63f53afe4ceeca00016bdd2f` |
| `email` | body | `string` | no | Update the contact email. Example: `example@email.com` |
| `website_url` | body | `string` | no | Update the employer website URL. Example: `https://www.apollo.io/` |
| `label_names[]` | body | `array<string>` | no | Replace lists this contact belongs to. (Passing new values will overwrite existing lists.) |
| `contact_stage_id` | body | `string` | no | Update the contact stage ID. Example: `6095a710bd01d100a506d4af` |
| `present_raw_address` | body | `string` | no | Update location (city/state/country). Example: `Atlanta, United States` |
| `direct_phone` | body | `string` | no | Primary phone. |
| `corporate_phone` | body | `string` | no | Work/office phone. |
| `mobile_phone` | body | `string` | no | Mobile phone. |
| `home_phone` | body | `string` | no | Home phone. |
| `other_phone` | body | `string` | no | Alternate phone. |
| `typed_custom_fields` | body | `object` | no | Add information to custom fields in Apollo. Your custom fields are unique to your team's Apollo account. This means that the examples in this documentation may not work for your testing purposes. To utilize this parameter successfully, call the Get a List of All Custom Fields endpoint and identify the `id` value for the custom field, as well as the appropriate data type. For example, if a custom field accepts picklist entries, you need to pass the accompanying `id` value for the picklist entry that you want to use as the input value. Example : When the Get a List of All Custom Fields endpoint returns an `id` of field: * `"60c39ed82bd02f01154c470a"` (datetime) then the value passed should be: `{"60c39ed82bd02f01154c470a": "2025-08-07"}` |
