# Decode Media Short Link with Watbot

Decodes a media short link in Watbot.

## Endpoint

- **Method:** `POST`
- **Path:** `/decodeShortLink`
- **Base URL:** `https://watbot.ru/api/v1`
- **Official documentation:** [Decode Media Short Link](https://docs.watbot.ru/rabota-s-api/ssylki-na-mediafaily)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Short media URL stored in a Watbot user variable. |
