# Search Subscribers by Custom Field with ManyChat

Finds subscribers in ManyChat by custom field.

## Endpoint

- **Method:** `GET`
- **Path:** `/fb/subscriber/findByCustomField`
- **Base URL:** `https://api.manychat.com`
- **Official documentation:** [Search Subscribers by Custom Field](https://api.manychat.com/swagger#/Subscriber/9fc380dcb49bb134b9405d4269896f56)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `field_id` | query | `number` | yes |
| `field_value` | query | `string` | yes |
