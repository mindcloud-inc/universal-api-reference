# Update Subscriber with SmartrMail

Updates an existing subscriber in SmartrMail.

## Endpoint

- **Method:** `PUT`
- **Path:** `/subscribers/:email_or_phone_or_uid`
- **Base URL:** `https://go.smartrmail.com/api/v1`
- **Official documentation:** [Update Subscriber](https://docs.smartrmail.com/en/articles/636619-manage-individual-subscribers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email_or_phone_or_uid` | path | `string` | yes | The subscriber email address, phone number, or UID. |
| `email` | body | `string` | no | The subscriber email address. |
| `phone` | body | `string` | no | The subscriber phone number. |
| `first_name` | body | `string` | no | The subscriber first name. |
| `last_name` | body | `string` | no | The subscriber last name. |
| `subscribed` | body | `boolean` | no | Whether the subscriber is currently subscribed. |
| `custom_fields` | body | `list<object>` | no | Custom field values to upsert on the subscriber. |
