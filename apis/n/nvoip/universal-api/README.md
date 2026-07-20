# <img src="https://images.mindcloud.co/apps/icons/nvoip_1775678204649.png" alt="Nvoip logo" width="28" height="28"> Nvoip: Universal API

Manage Nvoip calls, messages, and verification workflows

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/nvoip/latest
- **Category:** Support / Contact Center
- **Actions:** 11
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.nvoip.com.br
- **Vendor API docs:** https://nvoip.docs.apiary.io/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Balance](actions/get-balance.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nvoip/latest/actions/get-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (11)

### Access Token

| Action | Method | Description |
| --- | --- | --- |
| [Generate Access Token](actions/generate-access-token.md) | POST |  |

### Balance

| Action | Method | Description |
| --- | --- | --- |
| [Get Balance](actions/get-balance.md) | GET |  |

### Call

| Action | Method | Description |
| --- | --- | --- |
| [Create Call](actions/create-call.md) | POST |  |
| [End Call](actions/end-call.md) | DELETE |  |

### One-time Password

| Action | Method | Description |
| --- | --- | --- |
| [Check OTP](actions/check-otp.md) | GET |  |
| [Send OTP](actions/send-otp.md) | POST |  |

### Scheduled Sms

| Action | Method | Description |
| --- | --- | --- |
| [Delete Scheduled SMS](actions/delete-scheduled-sms.md) | DELETE |  |
| [List Scheduled SMS](actions/list-scheduled-sms.md) | GET |  |
| [Schedule SMS](actions/schedule-sms.md) | POST |  |

### Two-factor Authentication

| Action | Method | Description |
| --- | --- | --- |
| [Check 2FA Code](actions/check2fa-code.md) | GET |  |

### Voice Blast

| Action | Method | Description |
| --- | --- | --- |
| [Send Voice Blast](actions/send-voice-blast.md) | POST |  |

