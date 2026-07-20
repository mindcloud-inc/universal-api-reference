# Compare Documents (HTML JSON, Data URLs) with Diffchecker

Compares documents in Diffchecker and returns an HTML JSON diff from data URLs.

## Endpoint

- **Method:** `POST`
- **Path:** `/pdf`
- **Base URL:** `https://api.diffchecker.com/public`
- **Official documentation:** [Compare Documents (HTML JSON, Data URLs)](https://www.diffchecker.com/docs/document/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `left_pdf` | body | `string` | yes | Left PDF as a data URL. |
| `right_pdf` | body | `string` | yes | Right PDF as a data URL. |
