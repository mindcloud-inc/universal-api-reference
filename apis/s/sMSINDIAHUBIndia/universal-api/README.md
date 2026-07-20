# <img src="https://images.mindcloud.co/apps/icons/smsindiahub-icon_1776887118043.jpeg" alt="SMSINDIAHUB (India) logo" width="28" height="28"> SMSINDIAHUB (India): Universal API

SMSINDIAHUB (India) is an India-focused A2P messaging provider offering domestic HTTP SMS APIs that can authenticate with an API key, plus separate 2FA OTP endpoints with their own API-key flow.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sMSINDIAHUBIndia/latest
- **Category:** Marketing
- **Actions:** 11
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.smsindiahub.in/
- **Vendor API docs:** https://www.smsindiahub.in/api/india/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Check Balance](actions/check-balance.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMSINDIAHUBIndia/latest/actions/check-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (11)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Check Balance](actions/check-balance.md) | GET |  |

### Domestic Sms

| Action | Method | Description |
| --- | --- | --- |
| [Check Delivery Status](actions/check-delivery-status.md) | GET |  |
| [Schedule Promotional SMS](actions/schedule-promotional-sms.md) | POST |  |
| [Schedule Transactional SMS](actions/schedule-transactional-sms.md) | POST |  |
| [Send Group SMS](actions/send-group-sms.md) | POST |  |
| [Send Promotional Flash SMS](actions/send-promotional-flash-sms.md) | POST |  |
| [Send Promotional SMS](actions/send-promotional-sms.md) | POST |  |
| [Send Promotional Unicode SMS](actions/send-promotional-unicode-sms.md) | POST |  |
| [Send Transactional Flash SMS](actions/send-transactional-flash-sms.md) | POST |  |
| [Send Transactional SMS](actions/send-transactional-sms.md) | POST |  |
| [Send Transactional Unicode SMS](actions/send-transactional-unicode-sms.md) | POST |  |

