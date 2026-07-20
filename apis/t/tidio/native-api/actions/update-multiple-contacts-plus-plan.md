# Update Multiple Contacts [Plus plan] with Tidio

Updates multiple contacts in the Tidio workspace.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/contacts/batch`
- **Base URL:** `https://api.tidio.com`
- **Official documentation:** [Update Multiple Contacts [Plus plan]](https://developers.tidio.com/reference/patch_contacts-batch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contacts` | body | `list<object>` | yes | List of contacts to update. Maximum 100 per request. |
| `contacts[].id` | body | `string` | yes | Tidio contact UUID to update. |
| `contacts[].distinct_id` | body | `string` | no | External-system identifier for the contact. |
| `contacts[].email` | body | `string` | no | Contact email address. |
| `contacts[].first_name` | body | `string` | no | Contact first name. |
| `contacts[].last_name` | body | `string` | no | Contact last name. |
| `contacts[].phone` | body | `string` | no | Contact phone number. |
| `contacts[].email_consent` | body | `string` | no | Newsletter consent status for the contact. |
| `contacts[].properties` | body | `list<object>` | no | Optional list of custom contact properties. |
| `contacts[].properties[].name` | body | `string` | no | Name of the contact property. |
| `contacts[].properties[].value` | body | `string` | no | Value of the contact property. |
