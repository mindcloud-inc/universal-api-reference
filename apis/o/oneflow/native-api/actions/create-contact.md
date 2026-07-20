# Create Contact with Oneflow

Creates a contact in Oneflow.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts`
- **Base URL:** `https://api.oneflow.com/v1`
- **Official documentation:** [Create Contact](https://developer.oneflow.com/reference/create-a-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace_id` | body | `number` | yes | The workspace where the contact should be created. |
| `name` | body | `string` | no | The contact name. |
| `email` | body | `string` | no | The contact email. |
| `company_name` | body | `string` | no | The contact company name. |
| `phone_number` | body | `string` | no | The contact phone number. |
| `notes` | body | `string` | no | Notes for the contact. |
