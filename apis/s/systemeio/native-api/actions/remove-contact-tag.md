# Remove Contact Tag with Systeme.io

Removes a tag from a contact in Systeme.io.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/contacts/:id/tags/:tagId`
- **Base URL:** `https://api.systeme.io`
- **Official documentation:** [Remove Contact Tag](https://developer.systeme.io/reference/delete_contact_tag-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Contact identifier. |
| `tagId` | path | `string` | yes | Tag identifier. |
