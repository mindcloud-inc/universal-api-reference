# Sending Static Document with Dynamic Message with Picky Assist

## Endpoint

- **Method:** `POST`
- **Path:** `/push`
- **Base URL:** `https://app.pickyassist.com/api/v2`
- **Official documentation:** [Sending Static Document with Dynamic Message](https://help.pickyassist.com/api-documentation-v2/push-api/sending-media-attachments-push)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `application` | body | `string` | yes |
| `template_id` | body | `string` | yes |
| `template_header` | body | `string` | yes |
| `globalmedia` | body | `string` | yes |
| `data[]` | body | `array<object>` | yes |
