# Create Contact with BlueFox Email

Creates a contact in BlueFox Email.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/contacts/:projectId`
- **Base URL:** `https://api.bluefox.email`
- **Official documentation:** [Create Contact](https://bluefox.email/docs/api/contacts-management#create-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | BlueFox project ID. |
| `email` | body | `string` | yes | Email address for the new contact. |
| `name` | body | `string` | no | Name for the new contact. |
