# Create or Upsert Subscriber with MailerLite

Creates a subscriber in MailerLite, or updates one with the same email.

## Endpoint

- **Method:** `POST`
- **Path:** `/subscribers`
- **Base URL:** `https://connect.mailerlite.com/api`
- **Official documentation:** [Create or Upsert Subscriber](https://developers.mailerlite.com/docs/subscribers#create-upsert-subscriber)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Subscriber email address. |
| `fields` | body | `object` | no | Field values keyed by default or custom field name. |
| `groups[]` | body | `array<string>` | no | Existing group IDs to add the subscriber to. |
| `status` | body | `string` | no | Subscriber status. |
| `resubscribe` | body | `boolean` | no | Resubscribe previously unsubscribed subscribers when true. |
| `subscribed_at` | body | `string` | no | Subscription timestamp in yyyy-MM-dd HH:mm:ss format. |
| `ip_address` | body | `string` | no | Subscriber IP address. |
| `opted_in_at` | body | `string` | no | Opt-in timestamp in yyyy-MM-dd HH:mm:ss format. |
| `optin_ip` | body | `string` | no | Opt-in IP address. |
| `unsubscribed_at` | body | `string` | no | Unsubscribe timestamp in yyyy-MM-dd HH:mm:ss format. |
