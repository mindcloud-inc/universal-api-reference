# Create Contact with Heymarket SMS

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/contact`
- **Base URL:** `https://api.heymarket.com`
- **Official documentation:** [Create Contact](https://heymarket.docs.apiary.io/api-description-document)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `phone` | body | `string` | yes | Contact phone number in E.164 format without the plus sign. |
| `first` | body | `string` | no | Contact first name. |
| `last` | body | `string` | no | Contact last name. |
| `display_name` | body | `string` | no | Contact display name. |
| `email` | body | `string` | no | Contact email address. |
| `custom` | body | `object` | no | Contact custom fields object keyed by custom field id. |
| `avatar` | body | `string` | no | Avatar image URL. |
| `assignee_id` | body | `number` | no | Team member id to assign as the contact owner. |
| `tags[]` | body | `array<object>` | no | Array of tag objects to assign to the contact. |
| `tag_id` | body | `number` | no | Tag id within each tag object. |
| `is_opted_out` | body | `boolean` | no | Whether the contact is opted out of messaging. |
