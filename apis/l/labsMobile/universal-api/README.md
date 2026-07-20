# <img src="https://images.mindcloud.co/apps/icons/3a2a8e9a-e49b-4cef-b739-154a71e25594-8_1774974174251.png" alt="LabsMobile logo" width="28" height="28"> LabsMobile: Universal API

Send SMS messages, check account balance, and manage messaging operations through LabsMobile's SMS API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/labsMobile/latest
- **Category:** Communication / Team Messaging
- **Actions:** 17
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.labsmobile.com/
- **Vendor API docs:** https://www.labsmobile.com/en/sms-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Balance](actions/get-balance.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/labsMobile/latest/actions/get-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (17)

### Balance

| Action | Method | Description |
| --- | --- | --- |
| [Get Balance](actions/get-balance.md) | GET | Retrieves your LabsMobile account balance. |

### Certifiedsms

| Action | Method | Description |
| --- | --- | --- |
| [Send Certified SMS](actions/send-certified-sms.md) | POST | Sends a certified SMS message with LabsMobile. |

### Hlrresult

| Action | Method | Description |
| --- | --- | --- |
| [HLR Check](actions/hlr-check.md) | GET | Checks mobile number status and availability with LabsMobile HLR lookup. |

### Otpcode

| Action | Method | Description |
| --- | --- | --- |
| [Check OTP Code](actions/check-otp-code.md) | GET | Checks the status of an OTP code in LabsMobile. |
| [Resend OTP Code](actions/resend-otp-code.md) | POST | Resends an OTP code with LabsMobile. |
| [Send OTP Code](actions/send-otp-code.md) | POST | Creates and sends an OTP code with LabsMobile. |

### Otpenvironment

| Action | Method | Description |
| --- | --- | --- |
| [List OTP Environments](actions/list-otp-environments.md) | GET | Retrieves OTP environments from LabsMobile. |

### Scheduledsms

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Scheduled SMS](actions/cancel-scheduled-sms.md) | DELETE | Cancels a scheduled SMS message in LabsMobile. |
| [Schedule SMS](actions/schedule-sms.md) | POST | Schedules an SMS message in LabsMobile. |
| [Send Scheduled SMS Now](actions/send-scheduled-sms-now.md) | PUT | Sends a scheduled SMS message immediately in LabsMobile. |

### Smsbatch

| Action | Method | Description |
| --- | --- | --- |
| [Send Parameterized SMS](actions/send-parameterized-sms.md) | POST | Sends a parameterized SMS message with LabsMobile. |

### Smsmessage

| Action | Method | Description |
| --- | --- | --- |
| [Send Long SMS](actions/send-long-sms.md) | POST | Sends a concatenated long SMS message with LabsMobile. |
| [Send SMS](actions/send-sms.md) | POST | Sends an SMS message with LabsMobile. |
| [Send Test SMS](actions/send-test-sms.md) | POST | Sends a simulated SMS message with LabsMobile. |
| [Send Unicode SMS](actions/send-unicode-sms.md) | POST | Sends a Unicode SMS message with LabsMobile. |

### Smsprice

| Action | Method | Description |
| --- | --- | --- |
| [Get Country Prices](actions/get-country-prices.md) | GET | Retrieves SMS prices for specific countries from LabsMobile. |
| [Get Global Price List](actions/get-global-price-list.md) | GET | Retrieves the global SMS price list from LabsMobile. |

