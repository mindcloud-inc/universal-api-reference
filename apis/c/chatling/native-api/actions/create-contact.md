# Create Contact with Chatling

Creates a new contact in Chatling.

## Endpoint

- **Method:** `POST`
- **Path:** `/chatbots/:chatbotId/contacts`
- **Base URL:** `https://api.chatling.ai/v2`
- **Official documentation:** [Create Contact](https://docs.chatling.ai/api-reference/v2/contacts/create-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chatbotId` | path | `string` | yes | The chatbot ID. |
| `first_name` | body | `string` | no | The contact's first name. |
| `last_name` | body | `string` | no | The contact's last name. |
| `properties.email` | body | `string` | no | The contact's email address. |
| `properties.phone` | body | `string` | no | The contact's phone number. |
| `job_title` | body | `string` | no | The contact's job title. |
| `company_name` | body | `string` | no | The contact's company name. |
| `website_url` | body | `string` | no | The contact's website URL. |
| `properties.industry` | body | `string` | no | The contact's industry. |
| `properties.address` | body | `string` | no | The contact's address. |
| `properties.city` | body | `string` | no | The contact's city. |
| `properties.state` | body | `string` | no | The contact's state. |
| `postal_code` | body | `string` | no | The contact's postal code. |
| `properties.country` | body | `string` | no | The contact's country. |
