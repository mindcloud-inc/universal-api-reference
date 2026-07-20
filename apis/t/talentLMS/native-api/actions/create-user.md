# Create User with TalentLMS

Creates a new user in TalentLMS.

## Endpoint

- **Method:** `POST`
- **Path:** `/users`
- **Base URL:** `https://{domain}.talentlms.com/api/v2`
- **Official documentation:** [Create User](https://documenter.getpostman.com/view/31867199/2sAY548Kou#create-a-user)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | User first name. |
| `surname` | body | `string` | yes | User last name. |
| `login` | body | `string` | yes | Unique login username. |
| `email` | body | `string` | yes | User email address. |
| `password` | body | `string` | yes | Initial user password. |
| `timezone` | body | `string` | no | User timezone. |
| `locale` | body | `list` | no | User locale. Accepted values: `ar-AE`, `az-AZ`, `bs-BA`, `ca-ES`, `cs-CZ`, `da-DK`, `de-DE`, `el-GR`, `en-US`, `es-ES`, `et-EE`, `fa-IR`, `fi-FI`, `fr-FR`, `he-IL`, `hi-IN`, `hr-HR`, `hu-HU`, `hy-AM`, `id-ID`, `is-IS`, `it-IT`, `ja-JP`, `ka-GE`, `ko-KR`, `lt-LT`, `lv-LV`, `mn-MN`, `ms-MY`, `nb-NO`, `nl-NL`, `pl-PL`, `pt-BR`, `pt-PT`, `ro-RO`, `ru-RU`, `sk-SK`, `sl-SI`, `sr-RS`, `sv-SE`, `th-TH`, `tr-TR`, `uk-UA`, `vi-VN`, `zh-CN`, `zh-TW`. |
| `email_notifications` | body | `boolean` | no | Enable or disable email notifications. |
| `user_type_id` | body | `number` | no | User type identifier. |
| `status` | body | `boolean` | no | User status flag. |
| `description` | body | `string` | no | User description or bio. |
| `credits` | body | `number` | no | User credits balance. |
| `deactivation_date` | body | `string` | no | User deactivation date. |
