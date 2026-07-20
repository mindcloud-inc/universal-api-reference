# Update User with TalentLMS

Updates an existing user in TalentLMS.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/users/:id`
- **Base URL:** `https://{domain}.talentlms.com/api/v2`
- **Official documentation:** [Update User](https://documenter.getpostman.com/view/31867199/2sAY548Kou#update-a-user)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Numeric user ID. |
| `name` | body | `string` | no | Updated first name. |
| `surname` | body | `string` | no | Updated last name. |
| `login` | body | `string` | no | Updated login username. |
| `email` | body | `string` | no | Updated email address. |
| `description` | body | `string` | no | Updated user description. |
| `timezone` | body | `string` | no | Updated user timezone. |
| `locale` | body | `list` | no | Updated user locale. Accepted values: `ar-AE`, `az-AZ`, `bs-BA`, `ca-ES`, `cs-CZ`, `da-DK`, `de-DE`, `el-GR`, `en-US`, `es-ES`, `et-EE`, `fa-IR`, `fi-FI`, `fr-FR`, `he-IL`, `hi-IN`, `hr-HR`, `hu-HU`, `hy-AM`, `id-ID`, `is-IS`, `it-IT`, `ja-JP`, `ka-GE`, `ko-KR`, `lt-LT`, `lv-LV`, `mn-MN`, `ms-MY`, `nb-NO`, `nl-NL`, `pl-PL`, `pt-BR`, `pt-PT`, `ro-RO`, `ru-RU`, `sk-SK`, `sl-SI`, `sr-RS`, `sv-SE`, `th-TH`, `tr-TR`, `uk-UA`, `vi-VN`, `zh-CN`, `zh-TW`. |
| `email_notifications` | body | `boolean` | no | Enable or disable email notifications. |
| `user_type_id` | body | `number` | no | Updated user type id. |
| `status` | body | `string` | yes | User status (for example, active). |
| `deactivation_date` | body | `string` | no | Updated deactivation date. |
| `current_password` | body | `string` | no | Current password for password change. |
| `password` | body | `string` | no | Updated user password. |
| `credits` | body | `number` | no | Updated user credits. |
