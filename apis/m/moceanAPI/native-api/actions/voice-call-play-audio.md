# Voice Call Play Audio with Mocean API

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/2/voice/dial?mocean-resp-format=json&mocean-command=%5B%7B%22action%22%3A%22play%22%2C%22file%22%3A%22https%3A%2F%2Fwww.soundhelix.com%2Fexamples%2Fmp3%2FSoundHelix-Song-1.mp3%22%7D%5D`
- **Base URL:** `https://rest.moceanapi.com`
- **Official documentation:** [Voice Call Play Audio](https://moceanapi.com/docs#make-an-outbound-call)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mocean-to` | query | `string` | yes | Phone number to call, including country code. |
