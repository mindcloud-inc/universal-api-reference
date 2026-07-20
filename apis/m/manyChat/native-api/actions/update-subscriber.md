# Update Subscriber with ManyChat

Updates an existing subscriber in ManyChat.

## Endpoint

- **Method:** `POST`
- **Path:** `/fb/subscriber/updateSubscriber`
- **Base URL:** `https://api.manychat.com`
- **Official documentation:** [Update Subscriber](https://api.manychat.com/swagger#/Subscriber/3ab84a004f4a5942e7a5368c2b807d19)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `subscriber_id` | body | `number` | yes |
| `first_name` | body | `string` | no |
| `last_name` | body | `string` | no |
| `phone` | body | `string` | no |
| `email` | body | `string` | no |
| `gender` | body | `string` | no |
| `has_opt_in_sms` | body | `boolean` | no |
| `has_opt_in_email` | body | `boolean` | no |
| `consent_phrase` | body | `string` | no |
