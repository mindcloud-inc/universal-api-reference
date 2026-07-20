# Create Audience Member with DOOMSCROLLR

## Endpoint

- **Method:** `POST`
- **Path:** `/api/audience/create`
- **Base URL:** `https://mindcloudapps0402.doomscrollr.com`
- **Official documentation:** [Create Audience Member](https://doomscrollr.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | no | Audience member email address. |
| `email_md5` | body | `string` | no | MD5 hash of the lowercase email address when email is not provided. |
| `first_name` | body | `string` | no | Audience member first name. |
| `last_name` | body | `string` | no | Audience member last name. |
| `phone` | body | `string` | no | Audience member phone number. |
| `gender` | body | `string` | no | Audience member gender. |
| `source` | body | `string` | no | Source label for how the audience member was acquired. |
| `city` | body | `string` | no | Audience member city. |
| `state` | body | `string` | no | Audience member state or region. |
| `country` | body | `string` | no | Audience member country. |
| `bio` | body | `string` | no | Audience member biography or descriptor. |
| `username` | body | `string` | no | Audience member username or handle. |
| `followers` | body | `number` | no | Follower count for the audience member. |
| `tags[]` | body | `array<string>` | no | Tags to assign to the audience member. Send multiple values as a array. |
| `utm_source` | body | `string` | no | UTM source for the audience member attribution. |
| `utm_medium` | body | `string` | no | UTM medium for the audience member attribution. |
| `utm_campaign` | body | `string` | no | UTM campaign for the audience member attribution. |
| `utm_content` | body | `string` | no | UTM content value for the audience member attribution. |
| `utm_term` | body | `string` | no | UTM term value for the audience member attribution. |
| `created_at` | body | `string` | no | Optional created-at timestamp from the official Postman collection. |
