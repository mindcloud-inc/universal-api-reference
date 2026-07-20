# Sending Location with Picky Assist

## Endpoint

- **Method:** `POST`
- **Path:** `/push`
- **Base URL:** `https://app.pickyassist.com/api/v2`
- **Official documentation:** [Sending Location](https://help.pickyassist.com/api-documentation-v2/push-api/sending-location)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `application` | body | `string` | yes |
| `data[]` | body | `array<object>` | yes |
| `location` | body | `object` | yes |
