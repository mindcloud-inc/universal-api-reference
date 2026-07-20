# Quick Create Contact with CallKeeper

Creates a new contact quickly in CallKeeper.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts/quick`
- **Base URL:** `https://api.callkeeper.ai`
- **Official documentation:** [Quick Create Contact](https://api.callkeeper.ai/docs#/Contacts/quick_create_contact_contacts_quick_post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `first_name` | body | `string` | yes | Contact first name. |
| `phone` | body | `string` | yes | Contact phone number. |
