# Update Queue Schedule with Late

## Endpoint

- **Method:** `PUT`
- **Path:** `/queue/slots`
- **Base URL:** `https://zernio.com/api/v1`
- **Official documentation:** [Update Queue Schedule](https://docs.zernio.com/queue/update-schedule)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `profileId` | body | `string` | yes |
| `queueId` | body | `string` | no |
| `name` | body | `string` | no |
| `timezone` | body | `string` | yes |
| `slots[]` | body | `array<object>` | yes |
| `active` | body | `boolean` | no |
| `setAsDefault` | body | `boolean` | no |
| `reshuffleExisting` | body | `boolean` | no |
