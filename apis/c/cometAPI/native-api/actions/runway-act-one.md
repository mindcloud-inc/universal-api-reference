# Runway Act One with CometAPI

Creates a Runway Act-One transfer in CometAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/runway/pro/act_one`
- **Base URL:** `https://api.cometapi.com`
- **Official documentation:** [Runway Act One](https://apidoc.cometapi.com/api/video/runway/reverse-format/act-one-expression-migration)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `callback_url` | body | `string` | yes | Callback URL. |
| `image` | body | `string` | yes | Reference image. |
| `video` | body | `string` | yes | Source video. |
