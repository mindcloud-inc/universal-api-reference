# Upsert Audience Member with Mailchimp

Finds a member in Mailchimp, or creates one if no match is found.

## Endpoint

- **Method:** `PUT`
- **Path:** `lists/:list_id/members/:subscriber_hash`
- **Base URL:** `https://{serverPrefix}.api.mailchimp.com/3.0/`
- **Official documentation:** [Upsert Audience Member](https://us22.api.mailchimp.com/schema/3.0/Paths/Lists/Members/Instance.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email_address` | body | `string` | yes | Subscriber email address. |
| `email_type` | body | `string` | no | — |
| `interests` | body | `object` | no | — |
| `ip_opt` | body | `string` | no | — |
| `ip_signup` | body | `string` | no | — |
| `language` | body | `string` | no | — |
| `list_id` | path | `string` | yes | The unique ID for the Mailchimp audience. |
| `location` | body | `object` | no | — |
| `marketing_permissions[]` | body | `array<object>` | no | — |
| `merge_fields` | body | `object` | no | — |
| `skip_merge_validation` | query | `boolean` | no | — |
| `status` | body | `string` | no | — |
| `status_if_new` | body | `list<string>` | yes | Status to assign when creating a new member. Accepted values: `cleaned`, `pending`, `subscribed`, `transactional`, `unsubscribed`. |
| `subscriber_hash` | path | `string` | yes | MD5 hash of the lowercase subscriber email address. |
| `timestamp_opt` | body | `date` | no | — |
| `timestamp_signup` | body | `date` | no | — |
| `vip` | body | `boolean` | no | — |
