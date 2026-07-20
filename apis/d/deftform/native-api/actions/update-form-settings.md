# Update Form Settings with Deftform

Updates existing form settings in Deftform.

## Endpoint

- **Method:** `POST`
- **Path:** `/forms/:formId/settings`
- **Base URL:** `https://deftform.com/api/v1`
- **Official documentation:** [Update Form Settings](https://help.deftform.com/api/endpoints)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | The Deftform form ID whose settings should be updated. |
| `name` | body | `string` | no | New form name. Maximum 255 characters. Maximum length: 255. |
| `description` | body | `string` | no | Form description. Maximum 1000 characters. Maximum length: 1000. |
| `is_closed` | body | `boolean` | no | Whether the form is closed. |
| `responses_limit` | body | `number` | no | Optional response limit. Minimum 1. |
| `after_message` | body | `string` | no | Message shown after a submission. |
| `after_redirect_url` | body | `string` | no | URL to redirect respondents after submission. Maximum 500 characters. Maximum length: 500. |
| `cta_label` | body | `string` | no | Call-to-action label. Maximum 100 characters. Maximum length: 100. |
| `cta_label_continue` | body | `string` | no | Continue button label. Maximum 100 characters. Maximum length: 100. |
| `captcha` | body | `list<string>` | no | CAPTCHA provider: altcha, turnstile, recaptcha, or none. Accepted values: `0`, `1`, `2`, `3`. |
| `show_formtitle` | body | `boolean` | no | Whether to show the form title. |
| `seo_title` | body | `string` | no | SEO title. Maximum 255 characters. Maximum length: 255. |
| `seo_description` | body | `string` | no | SEO description. Maximum 500 characters. Maximum length: 500. |
