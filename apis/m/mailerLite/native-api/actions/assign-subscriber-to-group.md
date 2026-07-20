# Assign Subscriber to Group with MailerLite

Assigns an existing subscriber to a group in MailerLite.

## Endpoint

- **Method:** `POST`
- **Path:** `/subscribers/:subscriber_id/groups/:group_id`
- **Base URL:** `https://connect.mailerlite.com/api`
- **Official documentation:** [Assign Subscriber to Group](https://developers.mailerlite.com/docs/groups#assign-subscriber-to-a-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subscriber_id` | path | `string` | yes | Existing MailerLite subscriber identifier. |
| `group_id` | path | `string` | yes | Existing MailerLite group identifier. |
