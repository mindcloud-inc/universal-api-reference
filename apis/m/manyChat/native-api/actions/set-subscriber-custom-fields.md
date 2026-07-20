# Set Subscriber Custom Fields with ManyChat

Updates subscriber custom fields in ManyChat.

## Endpoint

- **Method:** `POST`
- **Path:** `/fb/subscriber/setCustomFields`
- **Base URL:** `https://api.manychat.com`
- **Official documentation:** [Set Subscriber Custom Fields](https://api.manychat.com/swagger#/Subscriber/4d01076149250e9e47f3b8aa7dc53baa)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `subscriber_id` | body | `number` | yes |
| `fields[]` | body | `array<object>` | yes |
