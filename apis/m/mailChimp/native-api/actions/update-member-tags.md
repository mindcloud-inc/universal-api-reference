# Update Member Tags with Mailchimp

Updates tags for a member in a Mailchimp audience.

## Endpoint

- **Method:** `POST`
- **Path:** `lists/:list_id/members/:subscriber_hash/tags`
- **Base URL:** `https://{serverPrefix}.api.mailchimp.com/3.0/`
- **Official documentation:** [Update Member Tags](https://us22.api.mailchimp.com/schema/3.0/Paths/Lists/Members/Tags.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `is_syncing` | body | `boolean` | no | Whether tag updates should sync. |
| `list_id` | path | `string` | yes | The unique ID for the Mailchimp audience. |
| `subscriber_hash` | path | `string` | yes | MD5 hash of the lowercase subscriber email address. |
| `tags[]` | body | `array<object>` | yes | Tag updates array. |
| `tags[].name` | body | `string` | yes | The merge tag name. |
| `tags[].status` | body | `list<string>` | yes | Whether the tag should be active or inactive. Accepted values: `active`, `inactive`. |
