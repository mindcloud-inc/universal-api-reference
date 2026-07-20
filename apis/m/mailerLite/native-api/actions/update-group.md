# Update Group with MailerLite

Updates an existing group in MailerLite.

## Endpoint

- **Method:** `PUT`
- **Path:** `/groups/:group_id`
- **Base URL:** `https://connect.mailerlite.com/api`
- **Official documentation:** [Update Group](https://developers.mailerlite.com/docs/groups#update-a-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `group_id` | path | `string` | yes | Existing MailerLite group identifier. |
| `name` | body | `string` | yes | New name for the MailerLite group. |
