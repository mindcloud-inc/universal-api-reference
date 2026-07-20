# Set Campaign Content with Mailchimp

Updates campaign content in Mailchimp.

## Endpoint

- **Method:** `PUT`
- **Path:** `campaigns/:campaign_id/content`
- **Base URL:** `https://{serverPrefix}.api.mailchimp.com/3.0/`
- **Official documentation:** [Set Campaign Content](https://us22.api.mailchimp.com/schema/3.0/Paths/Campaigns/Content/Instance.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `archive` | body | `object` | no | — |
| `campaign_id` | path | `string` | yes | The unique ID for the campaign. |
| `html` | body | `string` | no | HTML content. |
| `plain_text` | body | `string` | no | Plain-text content. |
| `template` | body | `object` | no | — |
| `url` | body | `string` | no | — |
| `variate_contents[]` | body | `array<object>` | no | — |
