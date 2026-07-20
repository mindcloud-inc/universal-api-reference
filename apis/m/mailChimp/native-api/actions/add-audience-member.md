# Add Audience Member with Mailchimp

Creates a new member in a Mailchimp audience.

## Endpoint

- **Method:** `POST`
- **Path:** `lists/:list_id/members`
- **Base URL:** `https://{serverPrefix}.api.mailchimp.com/3.0/`
- **Official documentation:** [Add Audience Member](https://us22.api.mailchimp.com/schema/3.0/Paths/Lists/Members/Collection.json)

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
| `status` | body | `list<string>` | yes | Subscription status. Accepted values: `cleaned`, `pending`, `subscribed`, `transactional`, `unsubscribed`. |
| `tags[]` | body | `array<string>` | no | — |
| `timestamp_opt` | body | `date` | no | — |
| `timestamp_signup` | body | `date` | no | — |
| `vip` | body | `boolean` | no | — |
