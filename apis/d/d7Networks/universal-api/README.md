# <img src="https://images.mindcloud.co/apps/icons/favicon-d7networks-com-48x48_1778172785161.png" alt="D7 Networks logo" width="28" height="28"> D7 Networks: Universal API

D7 Networks provides APIs for SMS, OTP verification, WhatsApp, Viber, and number lookup messaging workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/d7Networks/latest
- **Category:** Support / Contact Center
- **Actions:** 12
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://d7networks.com/
- **Vendor API docs:** https://d7networks.com/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get SMS Pricing](actions/get-sms-pricing.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/d7Networks/latest/actions/get-sms-pricing?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (12)

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Send SMS](actions/send-sms.md) | POST | Sends an SMS message with D7 Networks. |

### Otp

| Action | Method | Description |
| --- | --- | --- |
| [Resend OTP](actions/resend-otp.md) | POST | Resends a one-time password with D7 Networks. |
| [Send OTP](actions/send-otp.md) | POST | Sends a one-time password with D7 Networks. |

### Otp Report

| Action | Method | Description |
| --- | --- | --- |
| [Get OTP Status](actions/get-otp-status.md) | GET | Retrieves OTP verification status from D7 Networks. |

### Otp Verification

| Action | Method | Description |
| --- | --- | --- |
| [Verify OTP](actions/verify-otp.md) | POST | Verifies a one-time password with D7 Networks. |

### Phone Number Lookup

| Action | Method | Description |
| --- | --- | --- |
| [Get Number Lookup Status](actions/get-number-lookup-status.md) | GET | Retrieves number lookup status from D7 Networks. |

### Price

| Action | Method | Description |
| --- | --- | --- |
| [Get SMS Pricing](actions/get-sms-pricing.md) | GET | Retrieves SMS pricing details from D7 Networks. |

### Report

| Action | Method | Description |
| --- | --- | --- |
| [Get SMS Message Status](actions/get-sms-message-status.md) | GET | Retrieves SMS delivery status from D7 Networks. |

### Viber Message

| Action | Method | Description |
| --- | --- | --- |
| [Send Viber Message](actions/send-viber-message.md) | POST | Sends a Viber message with D7 Networks. |

### Viber Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Viber Message Status](actions/get-viber-message-status.md) | GET | Retrieves Viber message status from D7 Networks. |

### Whatsapp Message

| Action | Method | Description |
| --- | --- | --- |
| [Send WhatsApp Text Message](actions/send-whats-app-text-message.md) | POST | Sends a WhatsApp text message with D7 Networks. |

### Whatsapp Report

| Action | Method | Description |
| --- | --- | --- |
| [Get WhatsApp Message Status](actions/get-whats-app-message-status.md) | GET | Retrieves WhatsApp message status from D7 Networks. |

