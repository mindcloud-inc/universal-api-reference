# Get Grayscale Cat Placeholder with Placecats

## Endpoint

- **Method:** `GET`
- **Path:** `/g/:width/:height`
- **Base URL:** `https://placecats.com`
- **Official documentation:** [Get Grayscale Cat Placeholder](https://placecats.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `width` | path | `number` | yes | Required image width in pixels. |
| `height` | path | `number` | yes | Required image height in pixels. |
| `fit` | query | `string` | no | Optional fit: cover (default), contain, fill, inside, or outside. |
| `position` | query | `string` | no | Optional crop position: center (default), top, bottom, left, or right. |
