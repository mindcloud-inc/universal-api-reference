# <img src="https://images.mindcloud.co/apps/icons/s-msindiahub_1775144909181.png" alt="SMSINDIAHUB logo" width="28" height="28"> SMSINDIAHUB: Universal API

SMSINDIAHUB is an Indian A2P messaging provider offering domestic HTTP SMS APIs, a gated 2FA API, and a gated international SMS gateway.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sMSINDIAHUB/latest
- **Category:** Marketing
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.smsindiahub.in/
- **Vendor API docs:** https://www.smsindiahub.in/api/india/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Check Balance](actions/check-balance.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMSINDIAHUB/latest/actions/check-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### 2fa

| Action | Method | Description |
| --- | --- | --- |
| [Send 2FA OTP](actions/send2fa-otp.md) | POST | Sends an auto-generated SMS OTP in SMSINDIAHUB. |
| [Verify 2FA OTP](actions/verify2fa-otp.md) | GET | Retrieves SMS OTP verification results from SMSINDIAHUB. |

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Check Balance](actions/check-balance.md) | GET | Retrieves your SMS credit balance from SMSINDIAHUB. |

### Domestic Sms

| Action | Method | Description |
| --- | --- | --- |
| [Check Delivery Status](actions/check-delivery-status.md) | GET | Retrieves SMS delivery status from SMSINDIAHUB by message ID. |
| [Schedule Promotional SMS](actions/schedule-promotional-sms.md) | POST | Schedules a promotional SMS message in SMSINDIAHUB. |
| [Schedule Transactional SMS](actions/schedule-transactional-sms.md) | POST | Schedules a transactional SMS message in SMSINDIAHUB. |
| [Send Group SMS](actions/send-group-sms.md) | POST | Sends an SMS message to a group in SMSINDIAHUB. |
| [Send Promotional Flash SMS](actions/send-promotional-flash-sms.md) | POST | Sends a promotional flash SMS in SMSINDIAHUB. |
| [Send Promotional SMS](actions/send-promotional-sms.md) | POST | Sends a promotional SMS message in SMSINDIAHUB. |
| [Send Promotional Unicode SMS](actions/send-promotional-unicode-sms.md) | POST | Sends a promotional Unicode SMS in SMSINDIAHUB. |
| [Send Transactional Flash SMS](actions/send-transactional-flash-sms.md) | POST | Sends a transactional flash SMS in SMSINDIAHUB. |
| [Send Transactional SMS](actions/send-transactional-sms.md) | POST | Sends a transactional SMS message in SMSINDIAHUB. |
| [Send Transactional Unicode SMS](actions/send-transactional-unicode-sms.md) | POST | Sends a transactional Unicode SMS in SMSINDIAHUB. |

### International Sms

| Action | Method | Description |
| --- | --- | --- |
| [Send International Flash SMS](actions/send-international-flash-sms.md) | POST | Sends an international flash SMS in SMSINDIAHUB. |
| [Send International ISO-8859-1 Flash SMS](actions/send-international-iso88591-flash-sms.md) | POST | Sends an international ISO-8859-1 flash SMS in SMSINDIAHUB. |
| [Send International ISO-8859-1 Plain Text SMS](actions/send-international-iso88591-plain-text-sms.md) | POST | Sends an international ISO-8859-1 plain text SMS in SMSINDIAHUB. |
| [Send International Plain Text SMS](actions/send-international-plain-text-sms.md) | POST | Sends an international plain text SMS in SMSINDIAHUB. |
| [Send International Unicode Flash SMS](actions/send-international-unicode-flash-sms.md) | POST | Sends an international Unicode flash SMS in SMSINDIAHUB. |
| [Send International Unicode SMS](actions/send-international-unicode-sms.md) | POST | Sends an international Unicode SMS in SMSINDIAHUB. |
| [Send International WAP Push SMS](actions/send-international-wap-push-sms.md) | POST | Sends an international WAP Push SMS in SMSINDIAHUB. |

