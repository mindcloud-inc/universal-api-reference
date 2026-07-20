# <img src="https://images.mindcloud.co/apps/icons/voice-rssindependent-publisher_1777667330640.png" alt="VoiceRSS (Independent Publisher) logo" width="28" height="28"> VoiceRSS (Independent Publisher): Universal API

Convert text into speech audio with VoiceRSS

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/voiceRSSIndependentPublisher/latest
- **Category:** Marketing / Social Media
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.voicerss.org/
- **Vendor API docs:** https://www.voicerss.org/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Convert Text to Speech](actions/convert-text-to-speech.md):

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/voiceRSSIndependentPublisher/latest/actions/convert-text-to-speech" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "language": "en-us",
  "source_text": "Hello, world!"
}'
```

## Actions (1)

### Speech Audio

| Action | Method | Description |
| --- | --- | --- |
| [Convert Text to Speech](actions/convert-text-to-speech.md) | POST | Creates speech audio from text in VoiceRSS. |

