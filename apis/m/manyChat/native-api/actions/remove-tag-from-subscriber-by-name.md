# Remove Tag From Subscriber By Name with ManyChat

Removes a tag from a subscriber in ManyChat by name.

## Endpoint

- **Method:** `POST`
- **Path:** `/fb/subscriber/removeTagByName`
- **Base URL:** `https://api.manychat.com`
- **Official documentation:** [Remove Tag From Subscriber By Name](https://api.manychat.com/swagger#/Subscriber/59cef9685d8978968b28376db0123be4)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `subscriber_id` | body | `number` | yes |
| `tag_name` | body | `string` | yes |
