# Get Event with Schedule It

Retrieves event details from Schedule It.

## Endpoint

- **Method:** `GET`
- **Path:** `/events/:id`
- **Base URL:** `https://www.scheduleit.com/api`
- **Official documentation:** [Get Event](https://www.scheduleit.com/faq/10640/is-there-a-rest-api-or-webhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The event ID. |
| `fields` | query | `string` | no | Comma-separated list of fields to return. |
