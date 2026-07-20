# Run a fast OCR document scan with ID Analyzer

Creates a fast OCR document scan in ID Analyzer.

## Endpoint

- **Method:** `POST`
- **Path:** `/quickscan`
- **Base URL:** `https://api2.idanalyzer.com`
- **Official documentation:** [Run a fast OCR document scan](https://developer.idanalyzer.com/reference/post-quickscan-2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document` | body | `string` | yes | Base64-encoded document image. |
