# Modify a subscription with xMatters

Updates a subscription in your xMatters instance.

## Endpoint

- **Method:** `POST`
- **Path:** `subscriptions`
- **Base URL:** `https://mindcloud.xmatters.com/api/xm/1`
- **Official documentation:** [Modify a subscription](https://help.xmatters.com/xmapi/index.html#modify-a-subscription)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | body | `string` | no |
| `targetAllDevices` | body | `boolean` | no |
| `targetDeviceNames` | body | `list<string>` | no |
