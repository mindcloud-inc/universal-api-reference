# Delete Contact with BlueFox Email

Deletes a contact from BlueFox Email.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/contacts/:projectId/:contactEmailAddress`
- **Base URL:** `https://api.bluefox.email`
- **Official documentation:** [Delete Contact](https://bluefox.email/docs/api/contacts-management#delete-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | BlueFox project ID. |
| `contactEmailAddress` | path | `string` | yes | Email address of the contact to delete. |
