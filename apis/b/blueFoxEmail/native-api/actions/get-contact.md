# Get Contact with BlueFox Email

Retrieves a contact from BlueFox Email.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/contacts/:projectId/:contactEmailAddress`
- **Base URL:** `https://api.bluefox.email`
- **Official documentation:** [Get Contact](https://bluefox.email/docs/api/contacts-management#get-one-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | BlueFox project ID. |
| `contactEmailAddress` | path | `string` | yes | Email address of the contact to retrieve. |
