# Add Contact Tag with Systeme.io

Assigns a tag to a contact in Systeme.io.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/contacts/:id/tags`
- **Base URL:** `https://api.systeme.io`
- **Official documentation:** [Add Contact Tag](https://developer.systeme.io/reference/post_contact_tag-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Contact identifier |
| `tagId` | body | `number` | yes | Tag identifier to assign |
