# Remove Tag From Subscriber with ManyChat

Removes a tag from a subscriber in ManyChat.

## Endpoint

- **Method:** `POST`
- **Path:** `/fb/subscriber/removeTag`
- **Base URL:** `https://api.manychat.com`
- **Official documentation:** [Remove Tag From Subscriber](https://api.manychat.com/swagger#/Subscriber/09f35f7c1e6013311f36e3965dec650c)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `subscriber_id` | body | `number` | yes |
| `tag_id` | body | `number` | yes |
