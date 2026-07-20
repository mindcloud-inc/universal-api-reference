# Publish an opt-in page with Maildrip

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v1/opt-in-pages/{pageId}/publish`
- **Base URL:** `https://api.maildrip.io`
- **Official documentation:** [Publish an opt-in page](https://api.maildrip.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pageId` | path | `string` | yes | ID of the opt-in page to publish |
| `background_color` | body | `string` | no | Background color for the page |
| `banner_color` | body | `string` | no | Background color for the banner |
| `footer_color` | body | `string` | no | Background color for the footer |
| `heading` | body | `string` | no | Heading text for the page |
| `body` | body | `string` | no | Body text for the page |
| `facebook` | body | `string` | no | URL for social platform |
| `instagram` | body | `string` | no | URL of the social platform |
| `twitter` | body | `string` | no | URL for social platform |
| `linkedIn` | body | `string` | no | URL for social platform |
| `youtube` | body | `string` | no | URL for social platform |
| `tiktok` | body | `string` | no | URL for social platform |
| `button_text` | body | `string` | no | Text for the button |
| `button_bg_color` | body | `string` | no | Background color of the button |
| `button_redirect_link` | body | `string` | no | Redirect link for the button |
| `logo` | body | `string` | no | URL of page logo |
| `hero_image` | body | `string` | no | URL of page hero image |
| `template_id` | body | `string` | no | The template id |
| `business_mail` | body | `string` | no | Business mail of user |
| `phone_number` | body | `string` | no | Phone number of user |
| `form_fields[]` | body | `array<object>` | no | Array of form fields (optional) Send multiple values as a array. |
| `contact_groups[]` | body | `array<string>` | no | Array of contact group IDs (optional) Send multiple values as a array. |
| `page_url` | body | `string` | no | The custom opt-in page url |
