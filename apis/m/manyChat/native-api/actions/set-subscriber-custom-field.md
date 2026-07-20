# Set Subscriber Custom Field with ManyChat

Updates a subscriber custom field in ManyChat.

## Endpoint

- **Method:** `POST`
- **Path:** `/fb/subscriber/setCustomField`
- **Base URL:** `https://api.manychat.com`
- **Official documentation:** [Set Subscriber Custom Field](https://api.manychat.com/swagger#/Subscriber/81138a426b0903687848fdf8bdde6aa9)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `subscriber_id` | body | `number` | yes |
| `field_id` | body | `number` | yes |
| `field_value` | body | `string` | yes |
