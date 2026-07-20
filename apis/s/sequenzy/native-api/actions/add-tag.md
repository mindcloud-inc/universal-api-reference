# Add Tag with Sequenzy

Adds a tag to a subscriber in Sequenzy.

## Endpoint

- **Method:** `POST`
- **Path:** `/subscribers/tags`
- **Base URL:** `https://api.sequenzy.com/api/v1`
- **Official documentation:** [Add Tag](https://docs.sequenzy.com/api-reference/subscribers/tags/add)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Subscriber email address. |
| `tag` | body | `string` | yes | Tag name to add. |
