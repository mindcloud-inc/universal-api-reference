# Create Contact [Plus plan] with Tidio

Creates a contact in the Tidio workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts`
- **Base URL:** `https://api.tidio.com`
- **Official documentation:** [Create Contact [Plus plan]](https://developers.tidio.com/reference/post_contacts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `distinct_id` | body | `string` | yes | Custom unique contact identifier. |
| `email` | body | `string` | no | Contact email address. |
| `first_name` | body | `string` | no | Contact first name. |
| `last_name` | body | `string` | no | Contact last name. |
| `phone` | body | `string` | no | Contact phone number. |
| `email_consent` | body | `string` | no | Newsletter consent status for the contact. |
| `properties` | body | `list<object>` | no | Optional list of custom contact properties. |
| `properties[].name` | body | `string` | no | Name of the contact property. |
| `properties[].value` | body | `string` | no | Value of the contact property. |
