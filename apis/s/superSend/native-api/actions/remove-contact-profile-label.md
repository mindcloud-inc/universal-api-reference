# Remove Contact Profile Label with SuperSend

Deletes a profile label from a SuperSend contact.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/contacts/{id}/profile-labels/{labelId}`
- **Base URL:** `https://api.supersend.io/v2`
- **Official documentation:** [Remove Contact Profile Label](https://docs.supersend.io/docs/contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Resource ID (UUID) |
| `labelId` | path | `string` | yes | Label UUID to remove from the contact's profile |
