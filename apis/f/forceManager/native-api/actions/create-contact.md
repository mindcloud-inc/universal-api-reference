# Create Contact with ForceManager

Creates a new contact in ForceManager.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts`
- **Official documentation:** [Create Contact](https://support.forcemanager.net/en/articles/8613478-entity-types)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `gender` | body | `string` | yes | Gender of the contact. |
| `first_name` | body | `string` | yes | First name of the contact. |
| `last_name` | body | `string` | yes | Last name of the contact. |
| `email` | body | `string` | yes | Email address of the contact. |
