# Create a device with xMatters

Creates a device in your xMatters instance.

## Endpoint

- **Method:** `POST`
- **Path:** `devices`
- **Base URL:** `https://mindcloud.xmatters.com/api/xm/1`
- **Official documentation:** [Create a device](https://help.xmatters.com/xmapi/index.html#create-a-device)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `defaultDevice` | body | `boolean` | no |
| `delay` | body | `number` | no |
| `deviceType` | body | `string` | no |
| `name` | body | `string` | no |
| `owner` | body | `string` | no |
| `phoneNumber` | body | `string` | no |
| `priorityThreshold` | body | `string` | no |
| `recipientType` | body | `string` | no |
| `sequence` | body | `number` | no |
| `testStatus` | body | `string` | no |
| `timeframes` | body | `list<string>` | no |
