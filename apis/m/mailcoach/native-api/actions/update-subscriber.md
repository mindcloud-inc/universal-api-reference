# Update Subscriber with Mailcoach

Updates an existing subscriber in Mailcoach.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/subscribers/:uuid`
- **Base URL:** `https://mindcloud.mailcoach.app/api`
- **Official documentation:** [Update Subscriber](https://www.mailcoach.app/api-documentation/endpoints/subscribers/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `append_tags` | body | `boolean` | no | Append tags instead of replacing them. |
| `email` | body | `string` | yes | The subscriber email address. |
| `extra_attributes` | body | `object` | no | Additional subscriber attributes as an object. |
| `first_name` | body | `string` | no | The subscriber first name. |
| `last_name` | body | `string` | no | The subscriber last name. |
| `tags[]` | body | `array<string>` | no | Tags to sync or append to the subscriber. |
| `uuid` | path | `string` | yes | The UUID of the subscriber to update. |
