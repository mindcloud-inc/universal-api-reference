# Update Contact with BlueFox Email

Updates a contact in BlueFox Email.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/contacts/:projectId/:contactEmailAddress`
- **Base URL:** `https://api.bluefox.email`
- **Official documentation:** [Update Contact](https://bluefox.email/docs/api/contacts-management#update-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | BlueFox project ID. |
| `contactEmailAddress` | path | `string` | yes | Email address of the contact to update. |
| `email` | body | `string` | no | Updated email address for the contact. |
| `name` | body | `string` | no | Updated name for the contact. |
