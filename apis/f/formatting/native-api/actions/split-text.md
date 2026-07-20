# Split Text with Formatting

Splits text into segments in the Formatting app.

## Endpoint

- **Method:** `POST`
- **Path:** `/post`
- **Base URL:** `https://postman-echo.com`
- **Official documentation:** [Split Text](https://github.com/PipedreamHQ/pipedream/blob/master/components/formatting/actions/split-text/split-text.ts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input` | body | `string` | yes | The text to split. |
| `separator` | body | `string` | yes | The separator string. |
| `segmentIndex` | body | `number` | no | The zero-based segment index to return. |
