# VoiceShot: Native API Reference

A consolidated summary of VoiceShot's API configuration and 17 documented operations, with links to official documentation.

- **Official docs:** https://secure.voiceshot.com/docs/ivrapiv5/
- **API base URL:** `https://api.voiceshot.com`

## Authentication

### Basic

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

[Official authentication documentation](https://secure.voiceshot.com/docs/ivrapiv5/)

## API conventions

Request bodies use XML.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `text/xml` |

Responses from this API use XML.

## Endpoints (17 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Delete Pending Calls](actions/delete-pending-calls.md) | `POST /ivrapi.asp` | [docs](https://secure.voiceshot.com/docs/ivrapiv5/action.html) |
| [Delete Sound File](actions/delete-sound-file.md) | `POST /ivrapi.asp` | [docs](https://secure.voiceshot.com/docs/ivrapiv5/deletingsoundfiles.html) |
| [Pause Pending Calls](actions/pause-pending-calls.md) | `POST /ivrapi.asp` | [docs](https://secure.voiceshot.com/docs/ivrapiv5/action.html) |
| [Query Call By Call ID](actions/query-call-by-call-id.md) | `POST /ivrapi.asp` | [docs](https://secure.voiceshot.com/docs/ivrapiv5/callquery.html) |
| [Query Calls By Menu ID](actions/query-calls-by-menu-id.md) | `POST /ivrapi.asp` | [docs](https://secure.voiceshot.com/docs/ivrapiv5/callquery.html) |
| [Send Per-Recipient SMS Batch](actions/send-per-recipient-sms-batch.md) | `POST /ivrapi.asp` | [docs](https://secure.voiceshot.com/docs/ivrapiv5/txt.html) |
| [Send Per-Recipient TTS Voice Batch](actions/send-per-recipient-tts-voice-batch.md) | `POST /ivrapi.asp` | [docs](https://secure.voiceshot.com/docs/ivrapiv5/tts.html) |
| [Send Per-Recipient WAV Voice Batch](actions/send-per-recipient-wav-voice-batch.md) | `POST /ivrapi.asp` | [docs](https://secure.voiceshot.com/docs/ivrapiv5/outboundposts.html) |
| [Send SMS To Many Numbers](actions/send-sms-to-many-numbers.md) | `POST /ivrapi.asp` | [docs](https://secure.voiceshot.com/docs/ivrapiv5/txt.html) |
| [Send SMS To One Number](actions/send-sms-to-one-number.md) | `POST /ivrapi.asp` | [docs](https://secure.voiceshot.com/docs/ivrapiv5/txt.html) |
| [Send TTS Voice Call To Many Numbers](actions/send-tts-voice-call-to-many-numbers.md) | `POST /ivrapi.asp` | [docs](https://secure.voiceshot.com/docs/ivrapiv5/tts.html) |
| [Send TTS Voice Call To One Number](actions/send-tts-voice-call-to-one-number.md) | `POST /ivrapi.asp` | [docs](https://secure.voiceshot.com/docs/ivrapiv5/tts.html) |
| [Send WAV Voice Call To Many Numbers](actions/send-wav-voice-call-to-many-numbers.md) | `POST /ivrapi.asp` | [docs](https://secure.voiceshot.com/docs/ivrapiv5/filename.html) |
| [Send WAV Voice Call To One Number](actions/send-wav-voice-call-to-one-number.md) | `POST /ivrapi.asp` | [docs](https://secure.voiceshot.com/docs/ivrapiv5/filename.html) |
| [Test Configuration](actions/test-configuration.md) | `POST /ivrapi.asp` | [docs](https://secure.voiceshot.com/docs/ivrapiv5/action.html) |
| [Unpause Pending Calls](actions/unpause-pending-calls.md) | `POST /ivrapi.asp` | [docs](https://secure.voiceshot.com/docs/ivrapiv5/action.html) |
| [Upload Sound File](actions/upload-sound-file.md) | `POST /ivrapi.asp` | [docs](https://secure.voiceshot.com/docs/ivrapiv5/uploadingsoundfiles.html) |
