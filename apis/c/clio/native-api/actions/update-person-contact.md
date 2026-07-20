# Update Person Contact with Clio Manage

Updates a person contact in Clio Manage by contact ID.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/contacts/:id.json`
- **Base URL:** `https://app.clio.com/api/v4`
- **Official documentation:** [Update Person Contact](https://docs.developers.clio.com/clio-manage/api-reference/#tag/Contacts/operation/Contact%23update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | — |
| `data.first_name` | body | `string` | no | — |
| `data.last_name` | body | `string` | no | — |
| `data.email_addresses[0].address` | body | `string` | no | Email address to attach to the contact. |
| `data.email_addresses[0].name` | body | `list` | no | Label for the contact email address. Accepted values: `Home`, `Other`, `Work`. |
| `data.email_addresses[0].default_email` | body | `boolean` | no | Whether the email should be the default email on the contact. |
| `data.phone_numbers[0].number` | body | `string` | no | Phone number to attach to the contact. |
| `data.phone_numbers[0].name` | body | `list` | no | Label for the contact phone number. Accepted values: `Fax`, `Home`, `Mobile`, `Other`, `Pager`, `Skype`, `Work`. |
| `data.phone_numbers[0].default_number` | body | `boolean` | no | Whether the number should be the default phone number on the contact. |
