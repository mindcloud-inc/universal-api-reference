# Update Event with Schedule It

Updates an existing event in Schedule It.

## Endpoint

- **Method:** `POST`
- **Path:** `/events/:id`
- **Base URL:** `https://www.scheduleit.com/api`
- **Official documentation:** [Update Event](https://www.scheduleit.com/faq/10640/is-there-a-rest-api-or-webhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The event ID. |
| `title` | body | `string` | no | The updated event title. |
| `notes` | body | `string` | no | Updated notes for the event. |
