# Compare Images (JSON, Data URLs) with Diffchecker

Compares images in Diffchecker and returns a JSON diff from data URLs.

## Endpoint

- **Method:** `POST`
- **Path:** `/image`
- **Base URL:** `https://api.diffchecker.com/public`
- **Official documentation:** [Compare Images (JSON, Data URLs)](https://www.diffchecker.com/docs/image/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `left_image` | body | `string` | yes | Left image as a data URL. |
| `right_image` | body | `string` | yes | Right image as a data URL. |
