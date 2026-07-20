# Create Multiple Contacts with Sendblue

Creates multiple contacts in Sendblue.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/contacts/bulk`
- **Base URL:** `https://api.sendblue.co`
- **Official documentation:** [Create Multiple Contacts](https://docs.sendblue.com/api/resources/contacts/subresources/bulk/methods/create/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contacts[]` | body | `array<object>` | yes | Array of contact objects to create in bulk. |
| `contacts[].phone` | body | `string` | yes | Contact phone number in E.164 format. |
| `contacts[].first_name` | body | `string` | no | Contact's first name. |
| `contacts[].last_name` | body | `string` | no | Contact's last name. |
| `contacts[].company_name` | body | `string` | no | Company name. |
| `contacts[].custom_variables` | body | `object` | no | Custom key-value pairs for each contact. |
