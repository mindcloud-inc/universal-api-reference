# Update Audience with Mailchimp

Updates an existing audience in Mailchimp.

## Endpoint

- **Method:** `PATCH`
- **Path:** `lists/:list_id`
- **Base URL:** `https://{serverPrefix}.api.mailchimp.com/3.0/`
- **Official documentation:** [Update Audience](https://us22.api.mailchimp.com/schema/3.0/Paths/Lists/Instance.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `double_optin` | body | `boolean` | no | — |
| `list_id` | path | `string` | yes | The unique ID for the Mailchimp audience. |
| `marketing_permissions` | body | `boolean` | no | — |
| `notify_on_subscribe` | body | `string` | no | — |
| `notify_on_unsubscribe` | body | `string` | no | — |
| `use_archive_bar` | body | `boolean` | no | — |
| `name` | body | `string` | yes | Audience name. |
| `permission_reminder` | body | `string` | yes | Permission reminder shown in footer. |
| `email_type_option` | body | `boolean` | yes | Whether users can choose email type. |
| `contact` | body | `object` | yes | List contact object. |
| `campaign_defaults` | body | `object` | yes | Default campaign sender settings. |
| `contact.company` | body | `string` | yes | Company name. |
| `contact.address1` | body | `string` | yes | Primary street address. |
| `contact.city` | body | `string` | yes | City. |
| `contact.state` | body | `string` | yes | State or region. |
| `contact.zip` | body | `string` | yes | Postal code. |
| `contact.country` | body | `string` | yes | Two-letter country code. |
| `campaign_defaults.from_name` | body | `string` | yes | Default from name. |
| `campaign_defaults.from_email` | body | `string` | yes | Default from email address. |
| `campaign_defaults.subject` | body | `string` | yes | Default campaign subject. |
| `campaign_defaults.language` | body | `string` | yes | Default campaign language (for example en). |
