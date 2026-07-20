# Unassign Subscriber from Group with MailerLite

Removes a subscriber from a group in MailerLite.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/subscribers/:subscriber_id/groups/:group_id`
- **Base URL:** `https://connect.mailerlite.com/api`
- **Official documentation:** [Unassign Subscriber from Group](https://developers.mailerlite.com/docs/groups#unassign-subscriber-from-a-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subscriber_id` | path | `string` | yes | Existing MailerLite subscriber identifier. |
| `group_id` | path | `string` | yes | Existing MailerLite group identifier. |
