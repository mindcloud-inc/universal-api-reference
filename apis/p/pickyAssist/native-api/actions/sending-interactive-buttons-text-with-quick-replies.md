# Sending Interactive Buttons Text with Quick Replies with Picky Assist

## Endpoint

- **Method:** `POST`
- **Path:** `/push`
- **Base URL:** `https://app.pickyassist.com/api/v2`
- **Official documentation:** [Sending Interactive Buttons Text with Quick Replies](https://help.pickyassist.com/api-documentation-v2/push-api/sending-interactive-list-and-buttons)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `application` | body | `string` | yes |
| `template_id` | body | `string` | yes |
| `data[]` | body | `array<object>` | yes |
