# FraudLabs Pro: Native API Reference

A consolidated summary of FraudLabs Pro's API configuration and 9 documented operations, with links to official documentation.

- **Official docs:** https://www.fraudlabspro.com/developer/api/screen-order
- **API base URL:** `https://api.fraudlabspro.com/`

## Authentication

### API Key

Use your FraudLabs Pro API license key. FraudLabs Pro requires this key as the request field `key` on every API call.

### Credentials

- **API Key:** `apiKey` · required · Your FraudLabs Pro API license key. FraudLabs Pro sends this value as the request field `key` on each API call.

[Official authentication documentation](https://www.fraudlabspro.com/developer/api/screen-order)

## Endpoints (9 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Feedback Order](actions/feedback-order.md) | `POST v2/order/feedback` | [docs](https://www.fraudlabspro.com/developer/api/feedback-order) |
| [Feedback Payment](actions/feedback-payment.md) | `POST v2/payment/feedback` | [docs](https://www.fraudlabspro.com/developer/api/feedback-payment) |
| [Feedback User](actions/feedback-user.md) | `POST v2/user/feedback` | [docs](https://www.fraudlabspro.com/developer/api/feedback-user) |
| [Get Order Result](actions/get-order-result.md) | `GET v2/order/result` | [docs](https://www.fraudlabspro.com/developer/api/order-result) |
| [Get User Result](actions/get-user-result.md) | `GET v2/user/result` | [docs](https://www.fraudlabspro.com/developer/api/user-result) |
| [Get Verification Result](actions/get-verification-result.md) | `GET v2/verification/result` | [docs](https://www.fraudlabspro.com/developer/api/get-sms-verification-result) |
| [Screen Order](actions/screen-order.md) | `POST v2/order/screen` | [docs](https://www.fraudlabspro.com/developer/api/screen-order) |
| [Screen User](actions/screen-user.md) | `POST v2/user/screen` | [docs](https://www.fraudlabspro.com/developer/api/screen-user) |
| [Send SMS Verification](actions/send-sms-verification.md) | `POST v2/verification/send` | [docs](https://www.fraudlabspro.com/developer/api/send-sms-verification) |
