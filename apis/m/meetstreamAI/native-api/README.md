# Meetstream AI: Native API Reference

A consolidated summary of Meetstream AI's API configuration and 15 documented operations, with links to official documentation.

- **Official docs:** https://docs.meetstream.ai/api-reference
- **API base URL:** `https://api.meetstream.ai/api/v1`

## Authentication

### API Key

Connect Meetstream AI with an API key from the dashboard

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.meetstream.ai/api-reference/endpoint/post-create-bot)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `bots`. The next-page cursor is read from `nextCursor`.

## Pagination

Use `limit` in the query string to set the page size (default 50; accepted range 1–100). Use `cursor` in the query string as the pagination cursor.

## Endpoints (15 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Bot](actions/create-bot.md) | `POST /bots/create_bot` | [docs](https://docs.meetstream.ai/api-reference/ap-is/bot-endpoints/create-bot) |
| [Delete Scheduled Bot](actions/delete-scheduled-bot.md) | `DELETE /calendar/scheduled_bots/:bot_id` | [docs](https://docs.meetstream.ai/api-reference/ap-is/bot-endpoints/delete-scheduled-bot) |
| [Disable Cron](actions/disable-cron.md) | `POST /calendar/auto-schedule/disable` | [docs](https://docs.meetstream.ai/api-reference/ap-is/calendar/disable-cron) |
| [Get Audio Streams](actions/get-audio-streams.md) | `GET /bots/:bot_id/get_audio_streams` | [docs](https://docs.meetstream.ai/api-reference/ap-is/bot-endpoints/get-audio-streams) |
| [Get Bot Audio](actions/get-bot-audio.md) | `GET /bots/:bot_id/get_audio` | [docs](https://docs.meetstream.ai/api-reference/ap-is/bot-endpoints/get-bot-audio) |
| [Get Bot Chats](actions/get-bot-chats.md) | `GET /bots/:bot_id/get_chats` | [docs](https://docs.meetstream.ai/api-reference/ap-is/bot-endpoints/get-bot-chats) |
| [Get Bot Details](actions/get-bot-details.md) | `GET /bots/:bot_id/detail` | [docs](https://docs.meetstream.ai/api-reference/ap-is/bot-endpoints/get-bot-details) |
| [Get Bot Screenshots](actions/get-bot-screenshots.md) | `GET /bots/:bot_id/get_screenshots` | [docs](https://docs.meetstream.ai/api-reference/ap-is/bot-endpoints/get-bot-screenshots) |
| [Get Bot Status](actions/get-bot-status.md) | `GET /bots/:bot_id/status` | [docs](https://docs.meetstream.ai/api-reference/ap-is/bot-endpoints/get-bot-status) |
| [List Bots](actions/list-bots.md) | `GET /bots` | [docs](https://docs.meetstream.ai/api-reference/ap-is/bot-endpoints/list-bots) |
| [List Google Domains](actions/list-google-domains.md) | `GET /google-login-domains` | [docs](https://docs.meetstream.ai/api-reference/ap-is/google-signed-in-bots/list-google-domains) |
| [List Transcriptions](actions/list-transcriptions.md) | `GET /bots/:bot_id/transcriptions` | [docs](https://docs.meetstream.ai/api-reference/ap-is/transcription/get-bot-transcriptions) |
| [Remove Bot](actions/remove-bot.md) | `GET /bots/:bot_id/remove_bot` | [docs](https://docs.meetstream.ai/api-reference/ap-is/bot-endpoints/remove-bot) |
| [Reschedule Bot](actions/reschedule-bot.md) | `PATCH /calendar/scheduled_bots/:bot_id` | [docs](https://docs.meetstream.ai/api-reference/ap-is/bot-endpoints/reschedule-bot) |
| [Setup Cron](actions/setup-cron.md) | `POST /calendar/auto-schedule/enable` | [docs](https://docs.meetstream.ai/api-reference/ap-is/calendar/setup-cron) |
