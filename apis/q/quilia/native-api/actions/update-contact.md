# Update Contact with Quilia

## Endpoint

- **Method:** `PATCH`
- **Path:** `contacts/:id`
- **Base URL:** `https://api.quilia.dev/v2`
- **Official documentation:** [Update Contact](https://api.quilia.dev/v2#tag/contacts/PATCH/contacts/%7Bid%7D)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | no | The person's email address |
| `id` | path | `string` | yes | The unique identifier of the contact to update |
| `name` | body | `string` | no | The contact name |
| `phone` | body | `string` | no | The contact phone number |
| `type` | query | `list<string>` | yes | The type of contact to update Accepted values: `company`, `people`. |
