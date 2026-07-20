# WhyDonate: Native API Reference

A consolidated summary of WhyDonate's API configuration and 8 documented operations, with links to official documentation.

- **Official docs:** https://helpdesk.whydonate.com/en/category/donation-button-plugin-jwsieg/
- **API base URL:** `https://fundraiser.whydonate.dev`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
API-KEY: <apiKey>
```

[Official authentication documentation](https://helpdesk.whydonate.com/en/article/how-do-i-connect-my-whydonate-account-with-zapier-1yi1374/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (8 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Donation Values](actions/get-donation-values.md) | `GET /fundraiser/donation/values` | [docs](https://helpdesk.whydonate.com/en/article/how-to-set-up-the-wordpress-donation-form-plugin-1n3ep8d/) |
| [Get Fundraiser Details](actions/get-fundraiser-details.md) | `GET /fundraiser/get` | [docs](https://helpdesk.whydonate.com/en/article/how-to-set-up-the-wordpress-donation-form-plugin-1n3ep8d/) |
| [Get Payment Status](actions/get-payment-status.md) | `GET /fundraiser/payment/status/` | [docs](https://helpdesk.whydonate.com/en/article/how-to-set-up-the-wordpress-donation-form-plugin-1n3ep8d/) |
| [Get Widget Donation Values](actions/get-widget-donation-values.md) | `GET /fundraiser/wp/donation/values` | [docs](https://helpdesk.whydonate.com/en/article/how-to-set-up-the-wordpress-donation-form-plugin-1n3ep8d/) |
| [Get Widget Style](actions/get-widget-style.md) | `GET /fundraiser/user/style` | [docs](https://helpdesk.whydonate.com/en/article/how-to-set-up-the-wordpress-donation-form-plugin-1n3ep8d/) |
| [List User Fundraisers](actions/list-user-fundraisers.md) | `GET /fundraiser/wordpress/all` | [docs](https://helpdesk.whydonate.com/en/article/how-to-set-up-the-wordpress-donation-form-plugin-1n3ep8d/) |
| [List Widget Shortcodes](actions/list-widget-shortcodes.md) | `GET /fundraiser/styles/shortcodes` | [docs](https://helpdesk.whydonate.com/en/article/how-to-set-up-the-wordpress-donation-form-plugin-1n3ep8d/) |
| [List Widget Styles](actions/list-widget-styles.md) | `GET /fundraiser/styles` | [docs](https://helpdesk.whydonate.com/en/article/how-to-set-up-the-wordpress-donation-form-plugin-1n3ep8d/) |
