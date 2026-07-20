# Mocean API: Native API Reference

A consolidated summary of Mocean API's API configuration and 34 documented operations, with links to official documentation.

- **Official docs:** https://moceanapi.com/docs
- **API base URL:** `https://rest.moceanapi.com`

## Authentication

### API Token

Use a Mocean API Token. MindCloud sends it as Authorization: Bearer <token>.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://moceanapi.com/docs)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (34 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check Verify Code](actions/check-verify-code.md) | `POST /rest/2/verify/check?mocean-resp-format=json` | [docs](https://moceanapi.com/docs#verify-code) |
| [Create WhatsApp Template](actions/create-whatsapp-template.md) | `POST /template/whatsapp/message_templates` | [docs](https://moceanapi.com/docs#creating-whatsapp-template) |
| [Delete WhatsApp Template](actions/delete-whatsapp-template.md) | `DELETE /template/whatsapp/message_templates` | [docs](https://moceanapi.com/docs#delete-whatsapp-template-by-id) |
| [Download Recording](actions/download-recording.md) | `GET /rest/2/voice/rec` | [docs](https://moceanapi.com/docs#download-a-recording) |
| [Download WhatsApp Rich Media](actions/download-whatsapp-rich-media.md) | `GET /rest/2/media/whatsapp` | [docs](https://moceanapi.com/docs#download-rich-media) |
| [Edit WhatsApp Template](actions/edit-whatsapp-template.md) | `POST /template/whatsapp/:templateId` | [docs](https://moceanapi.com/docs#editing-whatsapp-template) |
| [Get Account Pricing](actions/get-account-pricing.md) | `GET /rest/2/account/pricing?mocean-resp-format=json` | [docs](https://moceanapi.com/docs#account-pricing) |
| [Get Balance](actions/get-balance.md) | `GET /rest/2/account/balance?mocean-resp-format=json` | [docs](https://moceanapi.com/docs#get-balance) |
| [Get Message Status](actions/get-message-status.md) | `GET /rest/2/report/message?mocean-resp-format=json` | [docs](https://moceanapi.com/docs#message-status) |
| [Get Number Lookup Pricing](actions/get-number-lookup-pricing.md) | `GET /rest/2/account/pricing?mocean-resp-format=json&mocean-type=number-lookup` | [docs](https://moceanapi.com/docs#account-pricing) |
| [Get SMS Pricing](actions/get-sms-pricing.md) | `GET /rest/2/account/pricing?mocean-resp-format=json&mocean-type=sms` | [docs](https://moceanapi.com/docs#account-pricing) |
| [Get Verify Pricing](actions/get-verify-pricing.md) | `GET /rest/2/account/pricing?mocean-resp-format=json&mocean-type=verify` | [docs](https://moceanapi.com/docs#account-pricing) |
| [Get WhatsApp Template](actions/get-whatsapp-template.md) | `GET /template/whatsapp/:templateId` | [docs](https://moceanapi.com/docs#get-template-by-id) |
| [Hang Up Call](actions/hang-up-call.md) | `POST /rest/2/voice/hangup?mocean-resp-format=json` | [docs](https://moceanapi.com/docs#hangup-a-call) |
| [List WhatsApp Templates](actions/list-whatsapp-templates.md) | `GET /template/whatsapp/message_templates` | [docs](https://moceanapi.com/docs#get-all-templates) |
| [Request Async Number Lookup](actions/request-async-number-lookup.md) | `POST /rest/2/nl?mocean-resp-format=json` | [docs](https://moceanapi.com/docs#request-number-lookup) |
| [Request Number Lookup](actions/request-number-lookup.md) | `POST /rest/2/nl?mocean-resp-format=json` | [docs](https://moceanapi.com/docs#request-number-lookup) |
| [Resend Verify Code SMS](actions/resend-verify-code-sms.md) | `POST /rest/2/verify/resend/sms?mocean-resp-format=json` | [docs](https://moceanapi.com/docs#resend-code-over-sms) |
| [Resend Verify Code SMS With Lookup](actions/resend-verify-code-sms-with-lookup.md) | `POST /rest/2/verify/resend/sms?mocean-resp-format=json&mocean-request-nl=1` | [docs](https://moceanapi.com/docs#resend-code-over-sms) |
| [Send Binary SMS](actions/send-binary-sms.md) | `POST /rest/2/sms?mocean-resp-format=json&mocean-coding=2` | [docs](https://moceanapi.com/docs#send-sms) |
| [Send Bulk SMS](actions/send-bulk-sms.md) | `POST /rest/2/sms?mocean-resp-format=json` | [docs](https://moceanapi.com/docs#send-sms) |
| [Send Flash SMS](actions/send-flash-sms.md) | `POST /rest/2/sms?mocean-resp-format=json&mocean-mclass=1&mocean-alt-dcs=1` | [docs](https://moceanapi.com/docs#send-sms) |
| [Send Scheduled SMS](actions/send-scheduled-sms.md) | `POST /rest/2/sms?mocean-resp-format=json` | [docs](https://moceanapi.com/docs#send-sms) |
| [Send SMS](actions/send-sms.md) | `POST /rest/2/sms?mocean-resp-format=json` | [docs](https://moceanapi.com/docs#send-sms) |
| [Send SMS With Delivery Report](actions/send-sms-with-delivery-report.md) | `POST /rest/2/sms?mocean-resp-format=json&mocean-dlr-mask=1` | [docs](https://moceanapi.com/docs#send-sms) |
| [Send Unicode SMS](actions/send-unicode-sms.md) | `POST /rest/2/sms?mocean-resp-format=json&mocean-charset=UTF-8` | [docs](https://moceanapi.com/docs#send-sms) |
| [Send Verify Code SMS](actions/send-verify-code-sms.md) | `POST /rest/2/verify/req/sms?mocean-resp-format=json` | [docs](https://moceanapi.com/docs#send-code-over-sms) |
| [Send Verify Code SMS With Lookup](actions/send-verify-code-sms-with-lookup.md) | `POST /rest/2/verify/req/sms?mocean-resp-format=json&mocean-request-nl=1` | [docs](https://moceanapi.com/docs#send-code-over-sms) |
| [Send Verify Code Telegram](actions/send-verify-code-telegram.md) | `POST /rest/2/verify/req/telegram?mocean-resp-format=json` | [docs](https://moceanapi.com/docs#send-code-over-telegram) |
| [Voice Call Collect Digits](actions/voice-call-collect-digits.md) | `POST /rest/2/voice/dial?mocean-resp-format=json&mocean-command=%5B%7B%22action%22%3A%22say%22%2C%22text%22%3A%22Press%201%20to%20continue%22%2C%22language%22%3A%22en-US%22%7D%2C%7B%22action%22%3A%22collect%22%2C%22eventUrl%22%3A%5B%22https%3A%2F%2Fexample.com%2Fcollect%22%5D%7D%5D` | [docs](https://moceanapi.com/docs#make-an-outbound-call) |
| [Voice Call Play Audio](actions/voice-call-play-audio.md) | `POST /rest/2/voice/dial?mocean-resp-format=json&mocean-command=%5B%7B%22action%22%3A%22play%22%2C%22file%22%3A%22https%3A%2F%2Fwww.soundhelix.com%2Fexamples%2Fmp3%2FSoundHelix-Song-1.mp3%22%7D%5D` | [docs](https://moceanapi.com/docs#make-an-outbound-call) |
| [Voice Call Record Call](actions/voice-call-record-call.md) | `POST /rest/2/voice/dial?mocean-resp-format=json&mocean-command=%5B%7B%22action%22%3A%22record%22%7D%2C%7B%22action%22%3A%22say%22%2C%22text%22%3A%22This%20call%20is%20being%20recorded%22%2C%22language%22%3A%22en-US%22%7D%5D` | [docs](https://moceanapi.com/docs#make-an-outbound-call) |
| [Voice Call Say Message](actions/voice-call-say-message.md) | `POST /rest/2/voice/dial?mocean-resp-format=json&mocean-command=%5B%7B%22action%22%3A%22say%22%2C%22text%22%3A%22Hello%20from%20MindCloud%22%2C%22language%22%3A%22en-US%22%7D%5D` | [docs](https://moceanapi.com/docs#make-an-outbound-call) |
| [Voice Call Transfer](actions/voice-call-transfer.md) | `POST /rest/2/voice/dial?mocean-resp-format=json&mocean-command=%5B%7B%22action%22%3A%22dial%22%2C%22to%22%3A%2260123456789%22%7D%5D` | [docs](https://moceanapi.com/docs#make-an-outbound-call) |
