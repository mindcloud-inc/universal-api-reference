# Create a subscription with xMatters

Creates a subscription in your xMatters instance.

## Endpoint

- **Method:** `POST`
- **Path:** `subscriptions`
- **Base URL:** `https://mindcloud.xmatters.com/api/xm/1`
- **Official documentation:** [Create a subscription](https://help.xmatters.com/xmapi/index.html#create-a-subscription)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `criteria` | body | `list<string>` | no |
| `description` | body | `string` | no |
| `form` | body | `string` | no |
| `name` | body | `string` | no |
| `notificationDelay` | body | `number` | no |
| `owner` | body | `string` | no |
| `recipients` | body | `list<string>` | no |
| `targetDeviceNames` | body | `list<string>` | no |
