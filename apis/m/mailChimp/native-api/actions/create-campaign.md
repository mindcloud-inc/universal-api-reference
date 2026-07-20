# Create Campaign with Mailchimp

Creates a new campaign in Mailchimp.

## Endpoint

- **Method:** `POST`
- **Path:** `campaigns`
- **Base URL:** `https://{serverPrefix}.api.mailchimp.com/3.0/`
- **Official documentation:** [Create Campaign](https://us22.api.mailchimp.com/schema/3.0/Paths/Campaigns/Collection.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content_type` | body | `string` | no | — |
| `rss_opts` | body | `object` | no | — |
| `social_card` | body | `object` | no | — |
| `tracking` | body | `object` | no | — |
| `type` | body | `list<string>` | yes | Campaign type. Accepted values: `absplit`, `plaintext`, `regular`, `rss`, `variate`. |
| `variate_settings` | body | `object` | no | — |
| `recipients` | body | `object` | no | Campaign recipients object. |
| `settings` | body | `object` | no | Campaign settings object. |
| `recipients.list_id` | body | `string` | yes | The unique audience (list) id for campaign recipients. |
| `settings.subject_line` | body | `string` | no | Campaign email subject line. |
| `settings.title` | body | `string` | no | Internal campaign title. |
| `settings.from_name` | body | `string` | no | From name used in campaign emails. |
| `settings.reply_to` | body | `string` | no | Reply-to email address. |
