# Compare Text (JSON) with Diffchecker

Compares text in Diffchecker and returns a JSON diff.

## Endpoint

- **Method:** `POST`
- **Path:** `/text`
- **Base URL:** `https://api.diffchecker.com/public`
- **Official documentation:** [Compare Text (JSON)](https://www.diffchecker.com/docs/text/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `left` | body | `string` | yes | The left text to compare. |
| `right` | body | `string` | yes | The right text to compare. |
