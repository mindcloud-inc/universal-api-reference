# Launch27: Native API Reference

A consolidated summary of Launch27's API configuration and 23 documented operations, with links to official documentation.

- **Official docs:** https://api.launch27.com/docs/
- **API base URL:** `https://{subdomain}.launch27.com/v1`

## Authentication

### Single Access Token

Connect with your Launch27 tenant subdomain, account email, and single access token.

### Credentials

- **Subdomain:** `subdomain` · required · Your Launch27 tenant subdomain, for example mindcloud-sandbox.
- **Email:** `email` · required · The email address tied to your Launch27 single access token.
- **API Key:** `apiKey` · required · Your Launch27 single access token.

[Official authentication documentation](https://docs.launch27.com/)

## Endpoints (23 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Authorize Billing Charge](actions/authorize-billing-charge.md) | `POST setup/billing/authorize_charge` | [docs](https://api.launch27.com/docs/) |
| [Check Gift Card Discount](actions/check-gift-card-discount.md) | `POST giftcard/discount` | [docs](https://api.launch27.com/docs/) |
| [Create Booking](actions/create-booking.md) | `POST booking` | [docs](https://api.launch27.com/docs/) |
| [Create Quote](actions/create-quote.md) | `POST quote` | [docs](https://api.launch27.com/docs/) |
| [Estimate Booking Price](actions/estimate-booking-price.md) | `POST booking/estimate_price` | [docs](https://api.launch27.com/docs/) |
| [Exchange FSPay Payment Account](actions/exchange-fspay-payment-account.md) | `POST fspay/token/exchange` | [docs](https://api.launch27.com/docs/) |
| [Get Billing Setup Intent](actions/get-billing-setup-intent.md) | `POST setup/billing/setup_intent` | [docs](https://api.launch27.com/docs/) |
| [Get Booking Form](actions/get-booking-form.md) | `GET booking/form` | [docs](https://api.launch27.com/docs/) |
| [Get Booking Quote](actions/get-booking-quote.md) | `POST booking/quote` | [docs](https://api.launch27.com/docs/) |
| [Get FSPay Token](actions/get-fspay-token.md) | `POST fspay/token` | [docs](https://api.launch27.com/docs/) |
| [Get General Settings](actions/get-general-settings.md) | `GET settings/general` | [docs](https://api.launch27.com/docs/) |
| [Get Invite Teams Policy](actions/get-invite-teams-policy.md) | `GET policy/invite_teams` | [docs](https://api.launch27.com/docs/) |
| [Get Location Policy](actions/get-location-policy.md) | `GET policy/location` | [docs](https://api.launch27.com/docs/) |
| [Get Quote Custom Fields](actions/get-quote-custom-fields.md) | `GET quote/custom_fields` | [docs](https://api.launch27.com/docs/) |
| [Get Quote Form](actions/get-quote-form.md) | `GET quote/form` | [docs](https://api.launch27.com/docs/) |
| [Get Recurring Policy](actions/get-recurring-policy.md) | `GET policy/recurring` | [docs](https://api.launch27.com/docs/) |
| [Get Settings](actions/get-settings.md) | `GET settings` | [docs](https://api.launch27.com/docs/) |
| [List Booking Custom Fields](actions/list-booking-custom-fields.md) | `GET booking/custom_fields` | [docs](https://api.launch27.com/docs/) |
| [List Booking Frequencies](actions/list-booking-frequencies.md) | `GET booking/frequencies` | [docs](https://api.launch27.com/docs/) |
| [List Booking Services](actions/list-booking-services.md) | `GET booking/services` | [docs](https://api.launch27.com/docs/) |
| [List Booking Spots](actions/list-booking-spots.md) | `POST booking/spots` | [docs](https://api.launch27.com/docs/) |
| [Purchase Gift Card](actions/purchase-gift-card.md) | `POST giftcard` | [docs](https://api.launch27.com/docs/) |
| [Search Booking Location](actions/search-booking-location.md) | `POST booking/location` | [docs](https://api.launch27.com/docs/) |
