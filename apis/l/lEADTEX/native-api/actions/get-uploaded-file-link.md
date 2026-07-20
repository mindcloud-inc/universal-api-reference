# Get Uploaded File Link with LEADTEX

Retrieves the original link for an uploaded media file in LEADTEX.

## Endpoint

- **Method:** `POST`
- **Path:** `/decodeShortLink?api_token={apiKey}`
- **Base URL:** `https://app.leadteh.ru/api/v1`
- **Official documentation:** [Get Uploaded File Link](https://docs.leadteh.ru/rabota-s-api/dopolnitelnye-metody/ssylki-na-mediafaily/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Short media file URL stored in a user variable. |
