# Subscribe User to List with Engage

Subscribes a user to a list in Engage, creating them if needed.

## Endpoint

- **Method:** `POST`
- **Path:** `/lists/:id/subscribers`
- **Base URL:** `https://api.engage.so/v1`
- **Official documentation:** [Subscribe User to List](https://docs.engage.so/en-us/a/62bbdd2e5bfea4dca4834045-lists#subscribe-user-to-a-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `created_at` | body | `string` | no | The creation date for the subscriber. |
| `email` | body | `string` | no | The subscriber’s email address. |
| `first_name` | body | `string` | no | The subscriber’s first name. |
| `id` | path | `string` | yes | The Engage list ID. |
| `last_name` | body | `string` | no | The subscriber’s last name. |
| `meta` | body | `object` | no | Additional subscriber attributes as an object. |
| `number` | body | `string` | no | The subscriber’s phone number in international format. |
