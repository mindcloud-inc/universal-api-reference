# Upsert Contact By Email Or Phone Number with Insighto.ai

## Endpoint

- **Method:** `POST`
- **Path:** `/contact/upsert`
- **Base URL:** `https://api.insighto.ai/api/v1`
- **Official documentation:** [Upsert Contact By Email Or Phone Number](https://docs.insighto.ai/api-reference/contact/upsert-contact-by-email-or-phone-number)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `first_name` | query | `string` | yes | Contact first name. |
| `last_name` | query | `string` | yes | Contact last name. |
| `email` | query | `string` | yes | Contact email address. |
| `phone_number` | query | `string` | yes | Contact phone number. |
