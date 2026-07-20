# Identify Contact with Salespanel

Identifies a contact in Salespanel by associating an email.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts/:contact_id/identify/`
- **Base URL:** `https://salespanel.io/api/v1`
- **Official documentation:** [Identify Contact](https://salespanel.io/docs/#identify-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | path | `string` | yes | The unique ID of the contact to identify. |
| `email` | body | `string` | yes | Email address for the contact. |
| `identified_through` | body | `string` | no | Source from where the email is acquired. |
