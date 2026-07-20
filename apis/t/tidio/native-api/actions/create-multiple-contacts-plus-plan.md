# Create Multiple Contacts [Plus plan] with Tidio

Creates multiple contacts in the Tidio workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts/batch`
- **Base URL:** `https://api.tidio.com`
- **Official documentation:** [Create Multiple Contacts [Plus plan]](https://developers.tidio.com/reference/post_contacts-batch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contacts` | body | `list<object>` | yes | List of contacts to create. Maximum 100 per request. |
| `contacts[].distinct_id` | body | `string` | yes | External-system identifier for the contact. |
| `contacts[].email` | body | `string` | no | Contact email address. |
| `contacts[].first_name` | body | `string` | no | Contact first name. |
| `contacts[].last_name` | body | `string` | no | Contact last name. |
| `contacts[].phone` | body | `string` | no | Contact phone number. |
| `contacts[].email_consent` | body | `string` | no | Newsletter consent status for the contact. |
| `contacts[].properties` | body | `list<object>` | no | Optional list of custom contact properties. |
| `contacts[].properties[].name` | body | `string` | no | Name of the contact property. |
| `contacts[].properties[].value` | body | `string` | no | Value of the contact property. |
