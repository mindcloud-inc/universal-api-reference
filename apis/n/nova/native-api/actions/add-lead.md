# Add Lead with Nova

## Endpoint

- **Method:** `POST`
- **Path:** `/rt/zapier/add/lead`
- **Base URL:** `https://app.n0va.com/v1/la`
- **Official documentation:** [Add Lead](https://app.n0va.com/documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list_id` | body | `number` | yes | Target Nova live list identifier. |
| `phone_number_concatenated` | body | `string` | yes | Lead phone number. Nova docs also allow an array, but this action currently models the common single-number case. |
| `firstname` | body | `string` | no | Lead first name. |
| `lastname` | body | `string` | no | Lead last name. |
| `email` | body | `string` | no | Lead email address. |
| `origin_crm_id` | body | `string` | no | External lead identifier in your CRM. |
| `statut` | body | `string` | no | Nova lead status label. |
| `assigned_to` | body | `string` | no | Nova user ID assigned to the lead. |
