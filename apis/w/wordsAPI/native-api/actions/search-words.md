# Search Words with WordsAPI

Finds words in WordsAPI by search criteria.

## Endpoint

- **Method:** `GET`
- **Path:** `/words`
- **Base URL:** `https://wordsapiv1.p.rapidapi.com`
- **Official documentation:** [Search Words](https://www.wordsapi.com/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hasDetails` | query | `string` | no | Return only words that contain a specific detail type. |
| `letterPattern` | query | `string` | no | Regex-like pattern to match words. |
| `partOfSpeech` | query | `string` | no | Restrict results by part of speech. |
| `soundsMax` | query | `string` | no | Maximum number of sounds. |
| `soundsMin` | query | `string` | no | Minimum number of sounds. |
