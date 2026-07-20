# Update Subscriber with MailerLite

Updates an existing subscriber in MailerLite.

## Endpoint

- **Method:** `PUT`
- **Path:** `/subscribers/:id`
- **Base URL:** `https://connect.mailerlite.com/api`
- **Official documentation:** [Update Subscriber](https://developers.mailerlite.com/docs/subscribers#update-a-subscriber)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Subscriber ID for the account. |
| `fields` | body | `object` | no | Field values keyed by default or custom field name. |
| `groups[]` | body | `array<string>` | no | Existing group IDs to keep on the subscriber. |
| `status` | body | `string` | no | Subscriber status. |
| `subscribed_at` | body | `string` | no | Subscription timestamp in yyyy-MM-dd HH:mm:ss format. |
| `ip_address` | body | `string` | no | Subscriber IP address. |
| `opted_in_at` | body | `string` | no | Opt-in timestamp in yyyy-MM-dd HH:mm:ss format. |
| `optin_ip` | body | `string` | no | Opt-in IP address. |
| `unsubscribed_at` | body | `string` | no | Unsubscribe timestamp in yyyy-MM-dd HH:mm:ss format. |
