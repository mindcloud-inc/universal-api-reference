# Vadootv: Native API Reference

A consolidated summary of Vadootv's API configuration and 15 documented operations, with links to official documentation.

- **Official docs:** https://docs.vadoo.tv/docs/intro/
- **API base URL:** `https://aiapi.vadoo.tv`

## Authentication

### API key

Authenticate Vadoo AI requests with the API key generated from the Vadoo AI profile page.

### Credentials

- **Vadoo AI API key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.vadoo.tv/docs/intro/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (15 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add captions](actions/add-captions.md) | `POST /api/add_captions` | [docs](https://docs.vadoo.tv/docs/guide/create-ai-captions) |
| [Create AI clips](actions/create-ai-clips.md) | `POST /api/create_ai_clips` | [docs](https://docs.vadoo.tv/docs/guide/create-ai-clips) |
| [Generate character image](actions/generate-character-image.md) | `POST /api/generate_character_image` | [docs](https://docs.vadoo.tv/docs/guide/ai-character/create-character-image) |
| [Generate podcast](actions/generate-podcast.md) | `POST /api/generate_podcast` | [docs](https://docs.vadoo.tv/docs/guide/create-an-ai-podcast) |
| [Generate video](actions/generate-video.md) | `POST /api/generate_video` | [docs](https://docs.vadoo.tv/docs/guide/ai-story/create-an-ai-video) |
| [Get all characters](actions/get-all-characters.md) | `GET /api/get_all_characters` | [docs](https://docs.vadoo.tv/docs/guide/ai-character/get-list-characters) |
| [Get background music](actions/get-background-music.md) | `GET /api/get_background_music` | [docs](https://docs.vadoo.tv/docs/guide/ai-story/get-list-background-music) |
| [Get character image](actions/get-character-image.md) | `GET /api/get_character_image` | [docs](https://docs.vadoo.tv/docs/guide/ai-character/get-character-image) |
| [Get languages](actions/get-languages.md) | `GET /api/get_languages` | [docs](https://docs.vadoo.tv/docs/guide/ai-story/get-list-languages) |
| [Get my balance](actions/get-my-balance.md) | `GET /api/get_my_balance` | [docs](https://docs.vadoo.tv/docs/guide/get-my-balance) |
| [Get styles](actions/get-styles.md) | `GET /api/get_styles` | [docs](https://docs.vadoo.tv/docs/guide/ai-story/get-list-styles) |
| [Get themes](actions/get-themes.md) | `GET /api/get_themes` | [docs](https://docs.vadoo.tv/docs/guide/ai-story/get-list-themes) |
| [Get topics](actions/get-topics.md) | `GET /api/get_topics` | [docs](https://docs.vadoo.tv/docs/guide/ai-story/get-list-video-topics) |
| [Get video URL](actions/get-video-url.md) | `GET /api/get_video_url` | [docs](https://docs.vadoo.tv/docs/guide/ai-story/get-video-url) |
| [Get voices](actions/get-voices.md) | `GET /api/get_voices` | [docs](https://docs.vadoo.tv/docs/guide/ai-story/get-list-voices) |
