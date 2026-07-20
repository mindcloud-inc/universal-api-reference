# Create Contact with CallKeeper

Creates a new contact in CallKeeper.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts`
- **Base URL:** `https://api.callkeeper.ai`
- **Official documentation:** [Create Contact](https://api.callkeeper.ai/docs#/Contacts/create_contact_contacts_post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `first_name` | body | `string` | yes | Contact first name. |
| `phone` | body | `string` | yes | Contact phone number. |
