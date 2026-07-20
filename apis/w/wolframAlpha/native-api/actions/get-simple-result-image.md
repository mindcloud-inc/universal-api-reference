# Get Simple Result Image with Wolfram Alpha

Retrieves a simple result image from Wolfram Alpha.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/simple`
- **Base URL:** `https://api.wolframalpha.com`
- **Official documentation:** [Get Simple Result Image](https://products.wolframalpha.com/simple-api/documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `background` | query | `string` | no | Image background color. |
| `foreground` | query | `string` | no | Image foreground color. |
| `i` | query | `string` | yes | Question or expression to render as a simple image result. |
| `width` | query | `number` | no | Image width in pixels. |
