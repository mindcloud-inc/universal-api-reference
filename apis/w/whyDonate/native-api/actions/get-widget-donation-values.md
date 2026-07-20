# Get Widget Donation Values with WhyDonate

## Endpoint

- **Method:** `GET`
- **Path:** `/fundraiser/wp/donation/values`
- **Base URL:** `https://fundraiser.whydonate.dev`
- **Official documentation:** [Get Widget Donation Values](https://helpdesk.whydonate.com/en/article/how-to-set-up-the-wordpress-donation-form-plugin-1n3ep8d/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `shortcode` | query | `string` | yes | Widget shortcode used by the WordPress/widget donation values endpoint. |
| `currency` | query | `string` | yes | Currency code selected in the widget before requesting donation values. |
| `mode` | query | `string` | no | Widget UI mode forwarded by the public script; the script falls back to form. |
