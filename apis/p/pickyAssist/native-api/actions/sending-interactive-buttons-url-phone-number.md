# Sending Interactive Buttons URL & Phone Number with Picky Assist

## Endpoint

- **Method:** `POST`
- **Path:** `/push`
- **Base URL:** `https://app.pickyassist.com/api/v2`
- **Official documentation:** [Sending Interactive Buttons URL & Phone Number](https://help.pickyassist.com/api-documentation-v2/push-api/sending-interactive-list-and-buttons)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `application` | body | `string` | yes |
| `template_id` | body | `string` | yes |
| `language` | body | `string` | yes |
| `interactive_globalbuttons[]` | body | `array<string>` | yes |
| `data[]` | body | `array<object>` | yes |
