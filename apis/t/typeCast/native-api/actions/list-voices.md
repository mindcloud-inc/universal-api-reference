# List Voices with TypeCast

Retrieves available voices from TypeCast.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/voices`
- **Base URL:** `https://api.typecast.ai/`
- **Official documentation:** [List Voices](https://typecast.ai/docs/api-reference/voices/list-voices)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model` | query | `list` | no | Filter voices by supported TTS model. Accepted values: `ssfm-v21`, `ssfm-v30`. |
| `gender` | query | `list` | no | Filter voices by gender. Accepted values: `female`, `male`. |
| `age` | query | `list` | no | Filter voices by age group. Accepted values: `child`, `elder`, `middle_age`, `teenager`, `young_adult`. |
| `use_cases` | query | `list` | no | Filter voices by use case category. Accepted values: `Ads`, `Anime`, `Announcer`, `Audiobook`, `Conversational`, `Documentary`, `E-learning`, `Game`, `News`, `Podcast`, `Rapper`, `Tiktok/Reels`, `Voicemail`. |
