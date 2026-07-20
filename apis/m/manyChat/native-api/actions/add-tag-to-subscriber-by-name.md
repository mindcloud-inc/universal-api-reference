# Add Tag To Subscriber By Name with ManyChat

Adds a tag to a subscriber in ManyChat by name.

## Endpoint

- **Method:** `POST`
- **Path:** `/fb/subscriber/addTagByName`
- **Base URL:** `https://api.manychat.com`
- **Official documentation:** [Add Tag To Subscriber By Name](https://api.manychat.com/swagger#/Subscriber/34ad004a12043ccbfee2faf1d290d30f)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `subscriber_id` | body | `number` | yes |
| `tag_name` | body | `string` | yes |
