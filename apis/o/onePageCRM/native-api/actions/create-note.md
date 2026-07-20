# Create Note with OnePageCRM

Creates a new note in OnePageCRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/notes`
- **Base URL:** `https://app.onepagecrm.com/api/v3`
- **Official documentation:** [Create Note](https://developer.onepagecrm.com/api/#/Notes/post_notes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | body | `string` | no | ID of the contact the note belongs to. |
| `text` | body | `string` | no | Extra details related to the note. Maximum length: 7168. |
| `date` | body | `string` | no | Creation date of the note in YYYY-MM-DD format. |
| `linked_deal_id` | body | `string` | no | Linked deal ID for the note. |
| `user_ids_to_notify[]` | body | `array<string>` | no | List of user IDs to notify. |
