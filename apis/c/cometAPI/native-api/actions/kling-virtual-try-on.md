# Kling Virtual Try On with CometAPI

Creates a Kling virtual try-on image in CometAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/kling/v1/images/kolors-virtual-try-on`
- **Base URL:** `https://api.cometapi.com`
- **Official documentation:** [Kling Virtual Try On](https://apidoc.cometapi.com/api/video/kling/virtual-try-on)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cloth_image` | body | `string` | yes | Clothing image. |
| `human_image` | body | `string` | yes | Human image. |
