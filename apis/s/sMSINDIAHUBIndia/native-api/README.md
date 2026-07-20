# SMSINDIAHUB (India): Native API Reference

A consolidated summary of SMSINDIAHUB (India)'s API configuration and 11 documented operations, with links to official documentation.

- **Official docs:** https://www.smsindiahub.in/api/india/
- **API base URL:** `https://cloud.smsindiahub.in`

## Authentication

### API Key

Use your SMSINDIAHUB domestic API key for the India SMS endpoints. The provider documentation says the India API can use `APIKey` instead of `user` and `password`.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.smsindiahub.in/where-can-i-find-my-api-key/)

## Endpoints (11 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check Balance](actions/check-balance.md) | `GET /vendorsms/CheckBalance.aspx` | [docs](https://www.smsindiahub.in/assets/pdf/Http-API-Document.pdf) |
| [Check Delivery Status](actions/check-delivery-status.md) | `GET /vendorsms/checkdelivery.aspx` | [docs](https://www.smsindiahub.in/assets/pdf/Http-API-Document.pdf) |
| [Schedule Promotional SMS](actions/schedule-promotional-sms.md) | `GET /vendorsms/pushsms.aspx` | [docs](https://www.smsindiahub.in/assets/pdf/Http-API-Document.pdf) |
| [Schedule Transactional SMS](actions/schedule-transactional-sms.md) | `GET /vendorsms/pushsms.aspx` | [docs](https://www.smsindiahub.in/assets/pdf/Http-API-Document.pdf) |
| [Send Group SMS](actions/send-group-sms.md) | `GET /vendorsms/pushsms.aspx` | [docs](https://www.smsindiahub.in/assets/pdf/Http-API-Document.pdf) |
| [Send Promotional Flash SMS](actions/send-promotional-flash-sms.md) | `GET /vendorsms/pushsms.aspx` | [docs](https://www.smsindiahub.in/assets/pdf/Http-API-Document.pdf) |
| [Send Promotional SMS](actions/send-promotional-sms.md) | `GET /vendorsms/pushsms.aspx` | [docs](https://www.smsindiahub.in/assets/pdf/Http-API-Document.pdf) |
| [Send Promotional Unicode SMS](actions/send-promotional-unicode-sms.md) | `GET /vendorsms/pushsms.aspx` | [docs](https://www.smsindiahub.in/assets/pdf/Http-API-Document.pdf) |
| [Send Transactional Flash SMS](actions/send-transactional-flash-sms.md) | `GET /vendorsms/pushsms.aspx` | [docs](https://www.smsindiahub.in/assets/pdf/Http-API-Document.pdf) |
| [Send Transactional SMS](actions/send-transactional-sms.md) | `GET /vendorsms/pushsms.aspx` | [docs](https://www.smsindiahub.in/assets/pdf/Http-API-Document.pdf) |
| [Send Transactional Unicode SMS](actions/send-transactional-unicode-sms.md) | `GET /vendorsms/pushsms.aspx` | [docs](https://www.smsindiahub.in/assets/pdf/Http-API-Document.pdf) |
