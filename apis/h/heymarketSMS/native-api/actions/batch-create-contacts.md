# Batch Create Contacts with Heymarket SMS

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/batch/contacts`
- **Base URL:** `https://api.heymarket.com`
- **Official documentation:** [Batch Create Contacts](https://heymarket.docs.apiary.io/api-description-document)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contacts[]` | body | `array<object>` | yes | Array of contacts to create. |
| `first` | body | `string` | no | First name. |
| `last` | body | `string` | no | Last name. |
| `display_name` | body | `string` | no | Display name. |
| `phone` | body | `string` | no | Phone number in E.164 format without the plus sign. |
| `email` | body | `string` | no | Email address. |
| `is_opted_out` | body | `boolean` | no | Whether the contact is opted out of messaging. |
| `overwrite` | query | `boolean` | no | Overwrite matching existing contacts. |
