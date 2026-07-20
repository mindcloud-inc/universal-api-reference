# Add Tag To Subscriber with ManyChat

Adds a tag to a subscriber in ManyChat.

## Endpoint

- **Method:** `POST`
- **Path:** `/fb/subscriber/addTag`
- **Base URL:** `https://api.manychat.com`
- **Official documentation:** [Add Tag To Subscriber](https://api.manychat.com/swagger#/Subscriber/ee797ad59ec8545bed43add11390b165)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `subscriber_id` | body | `number` | yes |
| `tag_id` | body | `number` | yes |
