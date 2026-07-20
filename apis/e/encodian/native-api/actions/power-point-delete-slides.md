# PowerPoint Delete Slides with Encodian

Deletes PowerPoint slides in Encodian.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/PowerPoint/PowerPointDeleteSlides`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [PowerPoint Delete Slides](https://support.encodian.com/hc/en-gb/articles/16535770370844)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileContent` | body | `string` | yes | The Base64 encoded content of the Microsoft PowerPoint file. |
| `startSlide` | body | `number` | no | Slide index where deletion starts. |
| `endSlide` | body | `number` | no | Slide index where deletion stops; defaults to the last slide. |
| `slideNumbers` | body | `string` | no | Comma-separated slide indexes to delete, such as 1,3,4. |
| `cultureName` | body | `string` | no | Culture name used when processing the request. |
