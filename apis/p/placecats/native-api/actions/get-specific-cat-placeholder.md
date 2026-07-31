# Get Specific Cat Placeholder with Placecats

## Endpoint

- **Method:** `GET`
- **Path:** `/:cat/:width/:height`
- **Base URL:** `https://placecats.com`
- **Official documentation:** [Get Specific Cat Placeholder](https://placecats.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cat` | path | `string` | yes | Required named-cat route value: neo, millie, millie_neo, neo_banana, neo_2, bella, poppy, or louie. |
| `width` | path | `number` | yes | Required image width in pixels. |
| `height` | path | `number` | yes | Required image height in pixels. |
| `fit` | query | `string` | no | Optional fit: cover (default), contain, fill, inside, or outside. |
| `position` | query | `string` | no | Optional crop position: center (default), top, bottom, left, or right. |
