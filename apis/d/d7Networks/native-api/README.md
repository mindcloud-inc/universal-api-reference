# D7 Networks: Native API Reference

A consolidated summary of D7 Networks's API configuration and 12 documented operations, with links to official documentation.

- **Official docs:** https://d7networks.com/docs/
- **API base URL:** `https://api.d7networks.com`

## Authentication

### D7 bearer token

Use a D7 Networks generated bearer token for API requests.

### Credentials

- **Auth token:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://d7networks.com/docs/authentication/overview/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (12 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Number Lookup Status](actions/get-number-lookup-status.md) | `GET /hlr/v1/report/:requestId` | [docs](https://d7networks.com/docs/number-lookup/get-status/) |
| [Get OTP Status](actions/get-otp-status.md) | `GET /verify/v1/report/:otpId` | [docs](https://d7networks.com/docs/verify/get-status/) |
| [Get SMS Message Status](actions/get-sms-message-status.md) | `GET /report/v1/message-log/:requestId` | [docs](https://d7networks.com/docs/sms/get-status/) |
| [Get SMS Pricing](actions/get-sms-pricing.md) | `GET /messages/v1/sms/pricing` | [docs](https://d7networks.com/docs/sms/pricing/) |
| [Get Viber Message Status](actions/get-viber-message-status.md) | `GET /report/v1/viber-log/:requestId` | [docs](https://d7networks.com/docs/viber/get-status/) |
| [Get WhatsApp Message Status](actions/get-whats-app-message-status.md) | `GET /whatsapp/v2/report/:requestId` | [docs](https://d7networks.com/docs/whatsapp/get-status/) |
| [Resend OTP](actions/resend-otp.md) | `POST /verify/v1/otp/resend-otp` | [docs](https://d7networks.com/docs/verify/resend-otp/) |
| [Send OTP](actions/send-otp.md) | `POST /verify/v1/otp/send-otp` | [docs](https://d7networks.com/docs/verify/send-otp/) |
| [Send SMS](actions/send-sms.md) | `POST /messages/v1/send` | [docs](https://d7networks.com/docs/sms/send-sms/) |
| [Send Viber Message](actions/send-viber-message.md) | `POST /viber/v1/send` | [docs](https://d7networks.com/docs/viber/send-viber-message/) |
| [Send WhatsApp Text Message](actions/send-whats-app-text-message.md) | `POST /whatsapp/v2/send` | [docs](https://d7networks.com/docs/whatsapp/send-message/text-message/) |
| [Verify OTP](actions/verify-otp.md) | `POST /verify/v1/otp/verify-otp` | [docs](https://d7networks.com/docs/verify/verify-otp/) |
