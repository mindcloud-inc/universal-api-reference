# Create Contact with Quilia

## Endpoint

- **Method:** `POST`
- **Path:** `contacts`
- **Base URL:** `https://api.quilia.dev/v2`
- **Official documentation:** [Create Contact](https://api.quilia.dev/v2#tag/contacts/POST/contacts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_data.email` | body | `string` | no | The person's email address |
| `contact_data.phone` | body | `string` | no | The contact phone number |
| `type` | body | `list<string>` | yes | The type of contact to create Accepted values: `company`, `people`. |
| `contact_data` | body | `object` | no | Contact data payload |
| `contact_data.name` | body | `string` | yes | The contact name |
