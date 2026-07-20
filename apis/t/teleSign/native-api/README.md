# TeleSign: Native API Reference

A consolidated summary of TeleSign's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://developer.telesign.com/enterprise/reference
- **API base URL:** `https://rest-ww.telesign.com`

## Authentication

### Basic Authentication

Use your TeleSign Customer ID as the username and your API Key as the password over HTTPS Basic authentication.

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

[Official authentication documentation](https://developer.telesign.com/enterprise/docs/authentication)

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check Phone Number Channel Capability](actions/check-phone-number-channel-capability.md) | `GET /capability/{channel}/{phone_number}` | [docs](https://developer.telesign.com/enterprise/reference/checkphonenumberchannelcapability) |
| [Check Phone Number RBM Capability](actions/check-phone-number-rbm-capability.md) | `GET /capability/rcs/{phone_number}/{agent_id}` | [docs](https://developer.telesign.com/enterprise/reference/checkphonenumberrbmcapability) |
| [Create Masked SMS Session](actions/create-masked-sms-session.md) | `POST /v1/anonymous/session/sms` | [docs](https://developer.telesign.com/enterprise/reference/createmaskedsmssession) |
| [Create Masked Voice SMS Session](actions/create-masked-voice-sms-session.md) | `POST /v1/anonymous/session/sms_voice` | [docs](https://developer.telesign.com/enterprise/reference/createmaskedvoicesmssession) |
| [Create Messaging Template](actions/create-messaging-template.md) | `POST /v1/omnichannel/templates` | [docs](https://developer.telesign.com/enterprise/reference/createmsgtemplate) |
| [End App Verify Call](actions/end-app-verify-call.md) | `POST /v1/verify/auto/voice/finalize` | [docs](https://developer.telesign.com/enterprise/reference/endappverifycall) |
| [Get All Messaging Templates](actions/get-all-messaging-templates.md) | `GET /v1/omnichannel/templates` | [docs](https://developer.telesign.com/enterprise/reference/getallmsgtemplates) |
| [Get App Verify Transaction Status](actions/get-app-verify-transaction-status.md) | `GET /v1/verify/auto/voice/{reference_id}` | [docs](https://developer.telesign.com/enterprise/reference/getappverifystatus) |
| [Get Messaging Template](actions/get-messaging-template.md) | `GET /v1/omnichannel/templates/{channel}/{name}` | [docs](https://developer.telesign.com/enterprise/reference/getmsgtemplate) |
| [Get Messaging Transaction Status](actions/get-messaging-transaction-status.md) | `GET /v1/omnichannel/{reference_id}` | [docs](https://developer.telesign.com/enterprise/reference/getmessagingstatus) |
| [Get Phone Live Status](actions/get-phone-live-status.md) | `GET /v1/phoneid/live/{complete_phone_number}` | [docs](https://developer.telesign.com/enterprise/reference/submitphonenumberforlivestatus) |
| [Get Recordings List By Date Range](actions/get-recordings-list-by-date-range.md) | `GET /v2/call_recording` | [docs](https://developer.telesign.com/enterprise/reference/getrecordingslistbydaterange) |
| [Get Recordings List For A Call](actions/get-recordings-list-for-a-call.md) | `GET /v2/call_recording/{reference_id}` | [docs](https://developer.telesign.com/enterprise/reference/getrecordingslistbycallid) |
| [Get SMS Transaction Status](actions/get-sms-transaction-status.md) | `GET /v1/messaging/{reference_id}` | [docs](https://developer.telesign.com/enterprise/reference/getsmsstatus) |
| [Get SMS Verify Transaction Status](actions/get-sms-verify-transaction-status.md) | `GET /v1/verify/{reference_id}` | [docs](https://developer.telesign.com/enterprise/reference/getsmsverifystatus) |
| [Get Voice Verify Transaction Status](actions/get-voice-verify-transaction-status.md) | `GET /v1/verify/{reference_id}` | [docs](https://developer.telesign.com/enterprise/reference/getvoiceverifystatus) |
| [Report SMS Completion](actions/report-sms-completion.md) | `PUT /v1/verify/completion/{reference_id}` | [docs](https://developer.telesign.com/enterprise/reference/reportsmscompletion) |
| [Report SMS Verify Completion](actions/report-sms-verify-completion.md) | `PUT /v1/verify/completion/{reference_id}` | [docs](https://developer.telesign.com/enterprise/reference/reportsmsverifycompletion) |
| [Report Unknown Caller ID](actions/report-unknown-caller-id.md) | `POST /v1/verify/auto/voice/finalize/callerid` | [docs](https://developer.telesign.com/enterprise/reference/reportappverifycallerid) |
| [Report Voice Verify Completion](actions/report-voice-verify-completion.md) | `PUT /v1/verify/completion/{reference_id}` | [docs](https://developer.telesign.com/enterprise/reference/reportvoiceverifycompletion) |
| [Request Phone Number Info](actions/request-phone-number-info.md) | `POST /v1/phoneid` | [docs](https://developer.telesign.com/enterprise/reference/submitphonenumberforidentityalt) |
| [Request Phone Number Info In Path](actions/request-phone-number-info-in-path.md) | `POST /v1/phoneid/{complete_phone_number}` | [docs](https://developer.telesign.com/enterprise/reference/submitphonenumberforidentity) |
| [Send Advanced Message](actions/send-advanced-message.md) | `POST /v1/omnichannel` | [docs](https://developer.telesign.com/enterprise/reference/sendadvancedmessage) |
| [Send App Verify Code](actions/send-app-verify-code.md) | `POST /v1/verify/auto/voice/initiate` | [docs](https://developer.telesign.com/enterprise/reference/sendappverifycode) |
| [Send Bulk SMS](actions/send-bulk-sms.md) | `POST /v1/verify/bulk_sms` | [docs](https://developer.telesign.com/enterprise/reference/sendbulksms) |
| [Send SMS Message](actions/send-sms-message.md) | `POST /v1/messaging` | [docs](https://developer.telesign.com/enterprise/reference/sendsms) |
| [Send SMS Verification Code](actions/send-sms-verification-code.md) | `POST /v1/verify/sms` | [docs](https://developer.telesign.com/enterprise/reference/sendsmsverifycode) |
| [Send Voice Action](actions/send-voice-action.md) | `POST /v2/voice` | [docs](https://developer.telesign.com/enterprise/reference/sendvoiceaction) |
| [Send Voice Verification Code](actions/send-voice-verification-code.md) | `POST /v1/verify/call` | [docs](https://developer.telesign.com/enterprise/reference/sendvoiceverifycode) |
| [Submit Phone Number For Intelligence](actions/submit-phone-number-for-intelligence.md) | `POST /v1/score/{complete_phone_number}` | [docs](https://developer.telesign.com/enterprise/reference/submitphonenumberforintelligence) |
