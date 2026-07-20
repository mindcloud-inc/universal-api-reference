# Create Queue Schedule with Late

## Endpoint

- **Method:** `POST`
- **Path:** `/queue/slots`
- **Base URL:** `https://zernio.com/api/v1`
- **Official documentation:** [Create Queue Schedule](https://docs.zernio.com/queue/create-schedule)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `profileId` | body | `string` | yes |
| `name` | body | `string` | yes |
| `timezone` | body | `string` | yes |
| `slots[]` | body | `array<object>` | yes |
| `active` | body | `boolean` | no |
