# LabsMobile: Native API Reference

A consolidated summary of LabsMobile's API configuration and 17 documented operations, with links to official documentation.

- **Official docs:** https://www.labsmobile.com/en/sms-api
- **API base URL:** `https://api.labsmobile.com`

## Authentication

### Basic Auth

Use your LabsMobile account email as the username and your generated API token as the password.

### Credentials

- **Registration email:** `username` · required
- **API token:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://www.labsmobile.com/en/sms-api/api-versions/http-rest-post-json)

## Endpoints (17 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Scheduled SMS](actions/cancel-scheduled-sms.md) | `POST /json/scheduled` | [docs](https://www.labsmobile.com/en/sms-api/api-versions/http-rest-post-json) |
| [Check OTP Code](actions/check-otp-code.md) | `GET /otp/checkCode` | [docs](https://www.labsmobile.com/en/sms-api/api-versions/sms-otp) |
| [Get Balance](actions/get-balance.md) | `GET /json/balance` | [docs](https://www.labsmobile.com/en/sms-api/api-versions/http-rest-post-json) |
| [Get Country Prices](actions/get-country-prices.md) | `POST /json/prices` | [docs](https://www.labsmobile.com/en/sms-api/api-versions/http-rest-post-json) |
| [Get Global Price List](actions/get-global-price-list.md) | `POST /json/prices` | [docs](https://www.labsmobile.com/en/sms-api/api-versions/http-rest-post-json) |
| [HLR Check](actions/hlr-check.md) | `GET /hlr` | [docs](https://www.labsmobile.com/en/sms-api/api-versions/hlr-check) |
| [List OTP Environments](actions/list-otp-environments.md) | `GET /otp/getEnvList` | [docs](https://www.labsmobile.com/en/sms-api/api-versions/sms-otp) |
| [Resend OTP Code](actions/resend-otp-code.md) | `GET /otp/resendCode` | [docs](https://www.labsmobile.com/en/sms-api/api-versions/sms-otp) |
| [Schedule SMS](actions/schedule-sms.md) | `POST /json/send` | [docs](https://www.labsmobile.com/en/sms-api/api-versions/http-rest-post-json) |
| [Send Certified SMS](actions/send-certified-sms.md) | `POST /json/send` | [docs](https://www.labsmobile.com/en/sms-api/api-versions/http-rest-post-json) |
| [Send Long SMS](actions/send-long-sms.md) | `POST /json/send` | [docs](https://www.labsmobile.com/en/sms-api/api-versions/http-rest-post-json) |
| [Send OTP Code](actions/send-otp-code.md) | `GET /otp/sendCode` | [docs](https://www.labsmobile.com/en/sms-api/api-versions/sms-otp) |
| [Send Parameterized SMS](actions/send-parameterized-sms.md) | `POST /json/send` | [docs](https://www.labsmobile.com/en/sms-api/api-versions/http-rest-post-json) |
| [Send Scheduled SMS Now](actions/send-scheduled-sms-now.md) | `POST /json/scheduled` | [docs](https://www.labsmobile.com/en/sms-api/api-versions/http-rest-post-json) |
| [Send SMS](actions/send-sms.md) | `POST /json/send` | [docs](https://www.labsmobile.com/en/sms-api/api-versions/http-rest-post-json) |
| [Send Test SMS](actions/send-test-sms.md) | `POST /json/send` | [docs](https://www.labsmobile.com/en/sms-api/api-versions/http-rest-post-json) |
| [Send Unicode SMS](actions/send-unicode-sms.md) | `POST /json/send` | [docs](https://www.labsmobile.com/en/sms-api/api-versions/http-rest-post-json) |
