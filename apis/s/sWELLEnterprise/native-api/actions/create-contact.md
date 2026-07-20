# Create Contact with SWELLEnterprise

Creates a new contact in SWELLEnterprise.

## Endpoint

- **Method:** `POST`
- **Path:** `/crm/contacts`
- **Base URL:** `https://dashboard.swellsystem.com/api/v1`
- **Official documentation:** [Create Contact](https://dashboard.swellsystem.com/docs#crm-contacts-POSTapi-v1-crm-contacts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `first_name` | body | `string` | yes | The contact's first name. |
| `last_name` | body | `string` | yes | The contact's last name. |
| `email` | body | `string` | no | The contact's email. |
| `phone` | body | `string` | no | The contact's phone. |
| `company_id` | body | `number` | no | The company ID. |
| `notes` | body | `string` | no | Notes about the contact. |
