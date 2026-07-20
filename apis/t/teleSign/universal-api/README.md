# <img src="https://images.mindcloud.co/apps/icons/images-8_1775150520665.png" alt="TeleSign logo" width="28" height="28"> TeleSign: Universal API

TeleSign provides messaging, phone verification, number intelligence, and identity APIs for customer engagement and fraud prevention.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/teleSign/latest
- **Category:** IT Operations / Security & Identity
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.telesign.com/
- **Vendor API docs:** https://developer.telesign.com/enterprise/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Check Phone Number Channel Capability](actions/check-phone-number-channel-capability.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teleSign/latest/actions/check-phone-number-channel-capability?connectionId=$CONNECTION_ID&channel=string&phoneNumber=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Create Messaging Template](actions/create-messaging-template.md) | POST |  |
| [Get All Messaging Templates](actions/get-all-messaging-templates.md) | GET |  |
| [Get Messaging Template](actions/get-messaging-template.md) | GET |  |
| [Get Messaging Transaction Status](actions/get-messaging-transaction-status.md) | GET |  |
| [Get Recordings List By Date Range](actions/get-recordings-list-by-date-range.md) | GET |  |
| [Get Recordings List For A Call](actions/get-recordings-list-for-a-call.md) | GET |  |
| [Get SMS Transaction Status](actions/get-sms-transaction-status.md) | GET |  |
| [Report SMS Completion](actions/report-sms-completion.md) | PUT |  |
| [Send Advanced Message](actions/send-advanced-message.md) | POST |  |
| [Send Bulk SMS](actions/send-bulk-sms.md) | POST |  |
| [Send SMS Message](actions/send-sms-message.md) | POST |  |
| [Send Voice Action](actions/send-voice-action.md) | POST |  |

### Phone Numbers

| Action | Method | Description |
| --- | --- | --- |
| [Check Phone Number Channel Capability](actions/check-phone-number-channel-capability.md) | GET |  |
| [Check Phone Number RBM Capability](actions/check-phone-number-rbm-capability.md) | GET |  |
| [Create Masked SMS Session](actions/create-masked-sms-session.md) | POST |  |
| [Create Masked Voice SMS Session](actions/create-masked-voice-sms-session.md) | POST |  |
| [End App Verify Call](actions/end-app-verify-call.md) | PUT |  |
| [Get App Verify Transaction Status](actions/get-app-verify-transaction-status.md) | GET |  |
| [Get Phone Live Status](actions/get-phone-live-status.md) | GET |  |
| [Get SMS Verify Transaction Status](actions/get-sms-verify-transaction-status.md) | GET |  |
| [Get Voice Verify Transaction Status](actions/get-voice-verify-transaction-status.md) | GET |  |
| [Report SMS Verify Completion](actions/report-sms-verify-completion.md) | PUT |  |
| [Report Unknown Caller ID](actions/report-unknown-caller-id.md) | PUT |  |
| [Report Voice Verify Completion](actions/report-voice-verify-completion.md) | PUT |  |
| [Request Phone Number Info](actions/request-phone-number-info.md) | POST |  |
| [Request Phone Number Info In Path](actions/request-phone-number-info-in-path.md) | POST |  |
| [Send App Verify Code](actions/send-app-verify-code.md) | POST |  |
| [Send SMS Verification Code](actions/send-sms-verification-code.md) | POST |  |
| [Send Voice Verification Code](actions/send-voice-verification-code.md) | POST |  |
| [Submit Phone Number For Intelligence](actions/submit-phone-number-for-intelligence.md) | POST |  |

