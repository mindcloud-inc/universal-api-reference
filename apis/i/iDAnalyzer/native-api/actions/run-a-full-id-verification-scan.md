# Run a full ID verification scan with ID Analyzer

Creates a full ID verification scan in ID Analyzer.

## Endpoint

- **Method:** `POST`
- **Path:** `/scan`
- **Base URL:** `https://api2.idanalyzer.com`
- **Official documentation:** [Run a full ID verification scan](https://developer.idanalyzer.com/reference/post-scan)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document` | body | `string` | yes | Base64-encoded document image. |
| `profile` | body | `string` | yes | KYC profile ID or preset profile alias. |
