# Create Subscriber with ManyChat

Creates a new subscriber in ManyChat.

## Endpoint

- **Method:** `POST`
- **Path:** `/fb/subscriber/createSubscriber`
- **Base URL:** `https://api.manychat.com`
- **Official documentation:** [Create Subscriber](https://api.manychat.com/swagger#/Subscriber/f42eb3580f33178fdf9d87f0c778f86e)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `first_name` | body | `string` | no |
| `last_name` | body | `string` | no |
| `phone` | body | `string` | no |
| `whatsapp_phone` | body | `string` | no |
| `email` | body | `string` | no |
| `gender` | body | `string` | no |
| `has_opt_in_sms` | body | `boolean` | no |
| `has_opt_in_email` | body | `boolean` | no |
| `consent_phrase` | body | `string` | no |
