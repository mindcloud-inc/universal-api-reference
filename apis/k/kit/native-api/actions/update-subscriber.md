# Update Subscriber with Kit

Updates an existing subscriber in Kit.

## Endpoint

- **Method:** `PUT`
- **Path:** `/subscribers/:id`
- **Base URL:** `https://api.kit.com/v4`
- **Official documentation:** [Update Subscriber](https://developers.kit.com/api-reference/subscribers/update-a-subscriber)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Subscriber ID. |
| `email_address` | body | `string` | no | Updated subscriber email address. |
| `state` | body | `list<string>` | no | Updated subscriber state. Accepted values: `active`, `bounced`, `cancelled`, `complained`, `inactive`. |
