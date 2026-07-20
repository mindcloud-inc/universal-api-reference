# Kling Video Effects with CometAPI

Creates a Kling video effects task in CometAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/kling/v1/videos/effects`
- **Base URL:** `https://api.cometapi.com`
- **Official documentation:** [Kling Video Effects](https://apidoc.cometapi.com/api/video/kling/video-effects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `effect_scene` | body | `string` | yes | Effect scene. |
| `input` | body | `object` | yes | Effect input payload. |
