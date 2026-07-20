# Create Contact with Nimble

Creates a new contact in Nimble.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/contact`
- **Base URL:** `https://app.nimble.com`
- **Official documentation:** [Create Contact](https://www.nimble.com/developers/docs/#tag/Contacts/operation/post-contact)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `record_type` | body | `string` | no |
| `fields` | body | `object` | yes |
| `is_important` | body | `boolean` | no |
