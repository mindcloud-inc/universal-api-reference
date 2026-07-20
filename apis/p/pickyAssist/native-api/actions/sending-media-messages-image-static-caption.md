# Sending Media Messages - Image Static Caption with Picky Assist

## Endpoint

- **Method:** `POST`
- **Path:** `/push`
- **Base URL:** `https://app.pickyassist.com/api/v2`
- **Official documentation:** [Sending Media Messages - Image Static Caption](https://help.pickyassist.com/api-documentation-v2/push-api/sending-media-attachments-push)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `priority` | body | `string` | no |
| `application` | body | `string` | yes |
| `globalmessage` | body | `string` | yes |
| `globalmedia` | body | `string` | yes |
| `data[]` | body | `array<object>` | yes |
