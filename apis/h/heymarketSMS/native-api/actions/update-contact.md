# Update Contact with Heymarket SMS

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/contact/:id`
- **Base URL:** `https://api.heymarket.com`
- **Official documentation:** [Update Contact](https://heymarket.docs.apiary.io/api-description-document)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Unique identifier of the contact. |
| `phone` | body | `string` | yes | Contact phone number in E.164 format without the plus sign. |
| `first` | body | `string` | no | First name. |
| `last` | body | `string` | no | Last name. |
| `display_name` | body | `string` | no | Display name for the contact. |
| `email` | body | `string` | no | Email address. |
| `custom` | body | `object` | no | Custom field values keyed by numeric custom field ID. |
| `avatar` | body | `string` | no | Avatar image URL. |
| `assignee_id` | body | `number` | no | Contact owner user ID. Use -1 to unassign. |
| `tags[]` | body | `array<object>` | no | Up to 5 contact tags. |
| `tag_id` | body | `number` | no | Tag identifier. |
| `is_opted_out` | body | `boolean` | no | Whether the contact is opted out of messaging. |
| `overwrite` | query | `boolean` | no | When true, replaces existing custom fields instead of merging them. |
