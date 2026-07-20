# Kling Image Expansion with CometAPI

Creates an expanded Kling image in CometAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/kling/v1/images/editing/expand`
- **Base URL:** `https://api.cometapi.com`
- **Official documentation:** [Kling Image Expansion](https://apidoc.cometapi.com/api/video/kling/image-expansion)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `image` | body | `string` | yes | Image input. |
| `right_expansion_ratio` | body | `number` | yes | Right expansion ratio. |
| `up_expansion_ratio` | body | `number` | yes | Upper expansion ratio. |
