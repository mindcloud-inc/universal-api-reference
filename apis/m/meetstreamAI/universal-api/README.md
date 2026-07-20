# <img src="https://images.mindcloud.co/apps/icons/cj-wr-qiqj6uyk1s5cs-zazht-idk0s_1776276875462.png" alt="Meetstream AI logo" width="28" height="28"> Meetstream AI: Universal API

Join meetings, capture transcripts, recordings, and meeting metadata

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/meetstreamAI/latest
- **Category:** Communication / Video Communications
- **Actions:** 15
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://meetstream.ai
- **Vendor API docs:** https://docs.meetstream.ai/api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Bots](actions/list-bots.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/meetstreamAI/latest/actions/list-bots?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (15)

### Bot

| Action | Method | Description |
| --- | --- | --- |
| [Create Bot](actions/create-bot.md) | POST | Creates a new bot in Meetstream AI. |
| [Delete Scheduled Bot](actions/delete-scheduled-bot.md) | DELETE | Deletes a scheduled bot from Meetstream AI. |
| [Get Audio Streams](actions/get-audio-streams.md) | GET | Retrieves bot audio streams from Meetstream AI. |
| [Get Bot Audio](actions/get-bot-audio.md) | GET | Retrieves bot audio from Meetstream AI. |
| [Get Bot Chats](actions/get-bot-chats.md) | GET | Retrieves bot chats from Meetstream AI. |
| [Get Bot Details](actions/get-bot-details.md) | GET | Retrieves bot details from Meetstream AI. |
| [Get Bot Screenshots](actions/get-bot-screenshots.md) | GET | Retrieves bot screenshots from Meetstream AI. |
| [Get Bot Status](actions/get-bot-status.md) | GET | Retrieves a bot status from Meetstream AI. |
| [List Bots](actions/list-bots.md) | GET | Retrieves bots from Meetstream AI. |
| [Remove Bot](actions/remove-bot.md) | DELETE | Deletes an active bot from Meetstream AI. |
| [Reschedule Bot](actions/reschedule-bot.md) | PUT | Updates a scheduled bot in Meetstream AI. |

### Google Domain

| Action | Method | Description |
| --- | --- | --- |
| [List Google Domains](actions/list-google-domains.md) | GET | Retrieves Google domains from Meetstream AI. |

### Schedules

| Action | Method | Description |
| --- | --- | --- |
| [Disable Cron](actions/disable-cron.md) | PUT | Updates calendar auto-scheduling in Meetstream AI. |
| [Setup Cron](actions/setup-cron.md) | PUT | Updates calendar auto-scheduling in Meetstream AI. |

### Transcription

| Action | Method | Description |
| --- | --- | --- |
| [List Transcriptions](actions/list-transcriptions.md) | GET | Retrieves bot transcriptions from Meetstream AI. |

