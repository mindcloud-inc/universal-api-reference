# Update Campaign with Mailchimp

Updates an existing campaign in Mailchimp.

## Endpoint

- **Method:** `PATCH`
- **Path:** `campaigns/:campaign_id`
- **Base URL:** `https://{serverPrefix}.api.mailchimp.com/3.0/`
- **Official documentation:** [Update Campaign](https://us22.api.mailchimp.com/schema/3.0/Paths/Campaigns/Instance.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign_id` | path | `string` | yes | The unique ID for the campaign. |
| `rss_opts` | body | `object` | no | — |
| `social_card` | body | `object` | no | — |
| `tracking` | body | `object` | no | — |
| `variate_settings` | body | `object` | no | — |
| `settings` | body | `object` | yes | Campaign settings object. |
| `recipients` | body | `object` | no | Campaign recipients object. |
| `settings.subject_line` | body | `string` | yes | Campaign email subject line. |
| `settings.from_name` | body | `string` | yes | From name used in campaign emails. |
| `settings.reply_to` | body | `string` | yes | Reply-to email address. |
| `recipients.list_id` | body | `string` | no | The unique audience (list) id for campaign recipients. |
