# Update Contact Properties [Plus plan] with Tidio

Updates a contact in the Tidio workspace.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/contacts/{contactId}`
- **Base URL:** `https://api.tidio.com`
- **Official documentation:** [Update Contact Properties [Plus plan]](https://developers.tidio.com/reference/patch_contacts-contactid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactId` | path | `string` | yes | The Tidio contact ID. |
| `email` | body | `string` | no | Contact email address. |
| `first_name` | body | `string` | no | Contact first name. |
| `last_name` | body | `string` | no | Contact last name. |
| `phone` | body | `string` | no | Contact phone number. |
| `email_consent` | body | `string` | no | Newsletter consent status for the contact. |
| `distinct_id` | body | `string` | no | Custom unique contact identifier. |
| `properties` | body | `list<object>` | no | Optional list of custom contact properties to patch. |
| `properties[].name` | body | `string` | no | Name of the contact property. |
| `properties[].value` | body | `string` | no | Value of the contact property. Leave empty when clearing the value upstream. |
