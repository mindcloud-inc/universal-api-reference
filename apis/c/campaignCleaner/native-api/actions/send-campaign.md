# Send Campaign with Campaign Cleaner

Submits a campaign for processing in Campaign Cleaner.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/send_campaign`
- **Base URL:** `https://api.campaigncleaner.com`
- **Official documentation:** [Send Campaign](https://docs.campaigncleaner.com/api-reference/endpoint/send-campaign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `send_campaign.campaign_html` | body | `string` | yes | The full HTML for the campaign to process. |
| `send_campaign.campaign_name` | body | `string` | yes | The campaign name. |
| `send_campaign.custom_info` | body | `string` | no | Optional metadata to store with the campaign. |
| `send_campaign.webhook_url` | body | `string` | no | Optional webhook URL to receive the completed campaign payload. |
| `send_campaign.adjust_font_colors` | body | `boolean` | no | Adjust bright font colors that can trigger spam filters. |
| `send_campaign.inline_css` | body | `boolean` | no | Inline CSS styles directly into HTML elements. |
| `send_campaign.remove_comments` | body | `boolean` | no | Remove CSS and HTML comments. |
| `send_campaign.remove_css_inheritance` | body | `boolean` | no | Remove inherited CSS after inlining. |
| `send_campaign.resize_and_host` | body | `boolean` | no | Resize and host eligible images on Campaign Cleaner CDN. |
| `send_campaign.remove_image_height` | body | `boolean` | no | Remove explicit image heights. |
