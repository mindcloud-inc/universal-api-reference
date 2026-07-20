# Create Message with Pachca (Admin)

Creates a new message in the Pachca Admin API.

## Endpoint

- **Method:** `POST`
- **Path:** `/messages`
- **Base URL:** `https://api.pachca.com/api/shared/v1`
- **Official documentation:** [Create Message](https://dev.pachca.com/api/messages/create)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `entity_type` | body | `string` | no |
| `entity_id` | body | `number` | yes |
| `content` | body | `string` | yes |
| `link_preview` | body | `boolean` | no |
