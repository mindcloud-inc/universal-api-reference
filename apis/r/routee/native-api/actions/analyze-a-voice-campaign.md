# Analyze a Voice Campaign with Routee

Analyzes a voice campaign in Routee.

## Endpoint

- **Method:** `POST`
- **Path:** `/voice/analysis`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Analyze a Voice Campaign](https://docs.routee.net/reference/analyze-a-voice-campaign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | body | `string` | yes | The sender id for this call |
| `groups[]` | body | `array<string>` | no | The groups of contacts selected as recipients of this call. One of "groups", "to", "contacts" parameters is required. |
| `contacts[]` | body | `array<string>` | no | The contacts selected as recipients of this call.  One of "groups", "to", "contacts" parameters is required. |
| `to[]` | body | `array<string>` | no | The recipients of this call, must be a list with valid numbers (mobiles or landlines). One of "groups", "to", "contacts" parameters is required. |
| `fileURL` | body | `string` | no | The url of the wav file to play |
| `message` | body | `object` | no | Represents the text message to be converted to wav file |
| `message.gender` | body | `string` | no | The gender of the voice message to be played |
| `message.language` | body | `string` | no | The language of the voice message to be played |
| `message.text` | body | `string` | no | The text of the voice message to be played |
