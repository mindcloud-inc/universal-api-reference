# Set Subscriber Custom Field By Name with ManyChat

Updates a subscriber custom field in ManyChat by name.

## Endpoint

- **Method:** `POST`
- **Path:** `/fb/subscriber/setCustomFieldByName`
- **Base URL:** `https://api.manychat.com`
- **Official documentation:** [Set Subscriber Custom Field By Name](https://api.manychat.com/swagger#/Subscriber/adc69e1e87197b5f31c80403a3913468)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `subscriber_id` | body | `number` | yes |
| `field_name` | body | `string` | yes |
| `field_value` | body | `string` | yes |
