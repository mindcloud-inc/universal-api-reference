# Compare Text (JSON, Default Word) with Diffchecker

Compares text in Diffchecker and returns a word-level JSON diff.

## Endpoint

- **Method:** `POST`
- **Path:** `/text`
- **Base URL:** `https://api.diffchecker.com/public`
- **Official documentation:** [Compare Text (JSON, Default Word)](https://www.diffchecker.com/docs/text/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `left` | body | `string` | yes | The left text to compare. |
| `right` | body | `string` | yes | The right text to compare. |
