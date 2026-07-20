# Create Subscriber with Mailcoach

Creates a new subscriber in a Mailcoach email list.

## Endpoint

- **Method:** `POST`
- **Path:** `/email-lists/:emailListUuid/subscribers`
- **Base URL:** `https://mindcloud.mailcoach.app/api`
- **Official documentation:** [Create Subscriber](https://www.mailcoach.app/api-documentation/endpoints/subscribers/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | The subscriber email address. |
| `emailListUuid` | path | `string` | yes | The UUID of the email list the subscriber should be added to. |
| `extra_attributes` | body | `object` | no | Additional subscriber attributes as an object. |
| `first_name` | body | `string` | no | The subscriber first name. |
| `last_name` | body | `string` | no | The subscriber last name. |
| `skip_confirmation` | body | `boolean` | no | Whether to skip the confirmation step. |
| `strict` | query | `boolean` | no | Fail instead of updating when the subscriber already exists. |
| `tags[]` | body | `array<string>` | no | Tags to sync onto the subscriber. |
