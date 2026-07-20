# Archive Audience Member with Mailchimp

Archives a member in a Mailchimp audience.

## Endpoint

- **Method:** `DELETE`
- **Path:** `lists/:list_id/members/:subscriber_hash`
- **Base URL:** `https://{serverPrefix}.api.mailchimp.com/3.0/`
- **Official documentation:** [Archive Audience Member](https://us22.api.mailchimp.com/schema/3.0/Paths/Lists/Members/Instance.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list_id` | path | `string` | yes | The unique ID for the Mailchimp audience. |
| `subscriber_hash` | path | `string` | yes | MD5 hash of the lowercase subscriber email address. |
