# WhatsApp Profile API with Picky Assist

## Endpoint

- **Method:** `POST`
- **Path:** `/update-profile`
- **Base URL:** `https://app.pickyassist.com/api/v2`
- **Official documentation:** [WhatsApp Profile API](https://help.pickyassist.com/api-documentation-v2/whatsapp-settings-apis/whatsapp-profile-api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `about` | body | `string` | no |
| `address` | body | `string` | no |
| `description` | body | `string` | no |
| `email` | body | `string` | no |
| `industry` | body | `number` | no |
| `websites[]` | body | `array<string>` | no |
| `profile_pic` | body | `string` | no |
