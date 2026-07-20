# Create Contact with ChatBotKit

## Endpoint

- **Method:** `POST`
- **Path:** `/contact/create`
- **Base URL:** `https://api.chatbotkit.com/v1`
- **Official documentation:** [Create Contact](https://chatbotkit.com/manuals/contacts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Name of the contact |
| `description` | body | `string` | no | Description of the contact |
| `meta` | body | `object` | no | Metadata for the contact |
| `fingerprint` | body | `string` | no | Fingerprint for the contact |
| `email` | body | `string` | no | Email address of the contact |
| `phone` | body | `string` | no | Phone number of the contact |
| `nick` | body | `string` | no | Nickname of the contact |
| `preferences` | body | `string` | no | Preferences of the contact |
| `verifiedAt` | body | `number` | no | Verification timestamp for the contact |
