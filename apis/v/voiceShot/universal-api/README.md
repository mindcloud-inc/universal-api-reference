# <img src="https://images.mindcloud.co/apps/icons/images_1775057532326.png" alt="VoiceShot logo" width="28" height="28"> VoiceShot: Universal API

VoiceShot provides inbound and outbound voice calling, IVR, SMS messaging, sound-file management, and real-time call-event integrations through an XML-over-HTTP API built around VoiceShot campaigns.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/voiceShot/latest
- **Category:** Support / Contact Center
- **Actions:** 17
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://voiceshot.com
- **Vendor API docs:** https://secure.voiceshot.com/docs/ivrapiv5/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Test Configuration](actions/test-configuration.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/voiceShot/latest/actions/test-configuration?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (17)

### Call

| Action | Method | Description |
| --- | --- | --- |
| [Delete Pending Calls](actions/delete-pending-calls.md) | DELETE | Deletes pending calls from a VoiceShot campaign. |
| [Query Call By Call ID](actions/query-call-by-call-id.md) | GET | Retrieves a call from VoiceShot by call ID. |
| [Query Calls By Menu ID](actions/query-calls-by-menu-id.md) | GET | Retrieves calls from VoiceShot by menu ID. |

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Pause Pending Calls](actions/pause-pending-calls.md) | PUT | Pauses pending calls in a VoiceShot campaign. |
| [Unpause Pending Calls](actions/unpause-pending-calls.md) | PUT | Resumes paused calls in a VoiceShot campaign. |

### Connection

| Action | Method | Description |
| --- | --- | --- |
| [Test Configuration](actions/test-configuration.md) | GET | Retrieves a configuration test result from VoiceShot. |

### Sms Message

| Action | Method | Description |
| --- | --- | --- |
| [Send Per-Recipient SMS Batch](actions/send-per-recipient-sms-batch.md) | POST | Creates per-recipient SMS messages in VoiceShot. |
| [Send SMS To Many Numbers](actions/send-sms-to-many-numbers.md) | POST | Creates SMS messages in VoiceShot for many recipients. |
| [Send SMS To One Number](actions/send-sms-to-one-number.md) | POST | Creates an SMS message in VoiceShot. |

### Sound File

| Action | Method | Description |
| --- | --- | --- |
| [Delete Sound File](actions/delete-sound-file.md) | DELETE | Deletes a sound file from VoiceShot. |
| [Upload Sound File](actions/upload-sound-file.md) | POST | Creates a sound file in VoiceShot. |

### Voice Call

| Action | Method | Description |
| --- | --- | --- |
| [Send Per-Recipient TTS Voice Batch](actions/send-per-recipient-tts-voice-batch.md) | POST | Creates per-recipient TTS voice calls in VoiceShot. |
| [Send Per-Recipient WAV Voice Batch](actions/send-per-recipient-wav-voice-batch.md) | POST | Creates per-recipient WAV voice calls in VoiceShot. |
| [Send TTS Voice Call To Many Numbers](actions/send-tts-voice-call-to-many-numbers.md) | POST | Creates TTS voice calls in VoiceShot for many recipients. |
| [Send TTS Voice Call To One Number](actions/send-tts-voice-call-to-one-number.md) | POST | Creates a TTS voice call in VoiceShot. |
| [Send WAV Voice Call To Many Numbers](actions/send-wav-voice-call-to-many-numbers.md) | POST | Creates WAV voice calls in VoiceShot for many recipients. |
| [Send WAV Voice Call To One Number](actions/send-wav-voice-call-to-one-number.md) | POST | Creates a WAV voice call in VoiceShot. |

