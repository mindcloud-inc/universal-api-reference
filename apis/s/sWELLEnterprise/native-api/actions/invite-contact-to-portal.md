# Invite Contact To Portal with SWELLEnterprise

Sends a portal invitation to a contact in SWELLEnterprise.

## Endpoint

- **Method:** `POST`
- **Path:** `/client-portal/contacts/:contactId/invite`
- **Base URL:** `https://dashboard.swellsystem.com/api/v1`
- **Official documentation:** [Invite Contact To Portal](https://dashboard.swellsystem.com/docs#client-portal-POSTapi-v1-client-portal-contacts--contactId--invite)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactId` | path | `number` | yes | The ID of the contact to invite. |
| `custom_message` | body | `string` | no | Optional custom message to include in the invitation email. |
