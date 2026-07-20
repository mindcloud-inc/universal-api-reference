# SMSINDIAHUB: Native API Reference

A consolidated summary of SMSINDIAHUB's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://www.smsindiahub.in/api/india/
- **API base URL:** `https://cloud.smsindiahub.in`

## Authentication

### Basic Username and Password

Use your SMSINDIAHUB account username and password. The provider expects these credentials in request query parameters rather than an Authorization header.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://m.smsindiahub.in/free-sms-gateway-developer-api/)

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check Balance](actions/check-balance.md) | `GET /vendorsms/CheckBalance.aspx` | [docs](https://www.smsindiahub.in/assets/pdf/Http-API-Document.pdf) |
| [Check Delivery Status](actions/check-delivery-status.md) | `GET /vendorsms/checkdelivery.aspx` | [docs](https://www.smsindiahub.in/assets/pdf/Http-API-Document.pdf) |
| [Schedule Promotional SMS](actions/schedule-promotional-sms.md) | `GET /vendorsms/pushsms.aspx` | [docs](https://www.smsindiahub.in/assets/pdf/Http-API-Document.pdf) |
| [Schedule Transactional SMS](actions/schedule-transactional-sms.md) | `GET /vendorsms/pushsms.aspx` | [docs](https://www.smsindiahub.in/assets/pdf/Http-API-Document.pdf) |
| [Send Group SMS](actions/send-group-sms.md) | `GET /vendorsms/pushsms.aspx` | [docs](https://www.smsindiahub.in/assets/pdf/Http-API-Document.pdf) |
| [Send International Flash SMS](actions/send-international-flash-sms.md) | `GET http://international.smsindiahub.in/bulksms/bulksms` | [docs](https://www.smsindiahub.in/assets/pdf/Int-API-Doc.pdf) |
| [Send International ISO-8859-1 Flash SMS](actions/send-international-iso88591-flash-sms.md) | `GET http://international.smsindiahub.in/bulksms/bulksms` | [docs](https://www.smsindiahub.in/assets/pdf/Int-API-Doc.pdf) |
| [Send International ISO-8859-1 Plain Text SMS](actions/send-international-iso88591-plain-text-sms.md) | `GET http://international.smsindiahub.in/bulksms/bulksms` | [docs](https://www.smsindiahub.in/assets/pdf/Int-API-Doc.pdf) |
| [Send International Plain Text SMS](actions/send-international-plain-text-sms.md) | `GET http://international.smsindiahub.in/bulksms/bulksms` | [docs](https://www.smsindiahub.in/assets/pdf/Int-API-Doc.pdf) |
| [Send International Unicode Flash SMS](actions/send-international-unicode-flash-sms.md) | `GET http://international.smsindiahub.in/bulksms/bulksms` | [docs](https://www.smsindiahub.in/assets/pdf/Int-API-Doc.pdf) |
| [Send International Unicode SMS](actions/send-international-unicode-sms.md) | `GET http://international.smsindiahub.in/bulksms/bulksms` | [docs](https://www.smsindiahub.in/assets/pdf/Int-API-Doc.pdf) |
| [Send International WAP Push SMS](actions/send-international-wap-push-sms.md) | `GET http://international.smsindiahub.in/bulksms/bulksms` | [docs](https://www.smsindiahub.in/assets/pdf/Int-API-Doc.pdf) |
| [Send Promotional Flash SMS](actions/send-promotional-flash-sms.md) | `GET /vendorsms/pushsms.aspx` | [docs](https://www.smsindiahub.in/assets/pdf/Http-API-Document.pdf) |
| [Send Promotional SMS](actions/send-promotional-sms.md) | `GET /vendorsms/pushsms.aspx` | [docs](https://www.smsindiahub.in/assets/pdf/Http-API-Document.pdf) |
| [Send Promotional Unicode SMS](actions/send-promotional-unicode-sms.md) | `GET /vendorsms/pushsms.aspx` | [docs](https://www.smsindiahub.in/assets/pdf/Http-API-Document.pdf) |
| [Send Transactional Flash SMS](actions/send-transactional-flash-sms.md) | `GET /vendorsms/pushsms.aspx` | [docs](https://www.smsindiahub.in/assets/pdf/Http-API-Document.pdf) |
| [Send Transactional SMS](actions/send-transactional-sms.md) | `GET /vendorsms/pushsms.aspx` | [docs](https://www.smsindiahub.in/assets/pdf/Http-API-Document.pdf) |
| [Send Transactional Unicode SMS](actions/send-transactional-unicode-sms.md) | `GET /vendorsms/pushsms.aspx` | [docs](https://www.smsindiahub.in/assets/pdf/Http-API-Document.pdf) |
| [Send 2FA OTP](actions/send2fa-otp.md) | `GET /api1.php/v1/{apiKey}/sms/{contactNo}/{emailId}` | [docs](https://www.smsindiahub.in/free-sms-gateway-developer-api/) |
| [Verify 2FA OTP](actions/verify2fa-otp.md) | `GET /verify.php/API/V1/{apiKey}/SMS/VERIFY/{otpTokenId}/{otp}` | [docs](https://www.smsindiahub.in/free-sms-gateway-developer-api/) |
